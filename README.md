# UFW TeamSpeak

TeamSpeak App Profile for UFW Firewall

## Ports that will be open

According the TeamSpeak [knowledgebase](https://support.teamspeakusa.com/index.php?/Knowledgebase/Article/View/44/16/which-ports-does-the-teamspeak-3-server-use), only the following ports will be allowed with this app profile !

| Service        | Protocol | Port  |
| -------------- | -------- | ----- |
| Voice          | UDP      | 9987  |
| Filetransfer   | TCP      | 30033 |
| ServerQuery    | TCP      | 10011 |
| TSDNS          | TCP      | 41144 |

## How-To

Simply download the TeamSpeak profile and move it to the UFW applications.d folder:

    wget -O teamspeak https://raw.githubusercontent.com/kmartin26/ufw-teamspeak/master/teamspeak
    sudo mv teamspeak /etc/ufw/applications.d/

Update the UFW App list:

    sudo ufw app update teamspeak

Then, we activate it:

    sudo ufw allow teamspeak

You're done!
