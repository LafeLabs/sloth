# [SLOTH!](https://github.com/LafeLabs/sloth)

![](https://raw.githubusercontent.com/LafeLabs/sloth/main/sloths/sloth1.png)


Self-replicating web pages sharing AI-generated sloth-themed art with the world!

Find any old computer that someone is getting rid of, it could be mac, pc or linux(but not Chromebook).  

You will need a thumb drive.  Follow the instructions below to install Ubuntu and wipe all the old data on the hard drive.

[https://ubuntu.com instructions](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview)

Once Ubuntu is installed, open a command line and type:

```
sudo apt update
sudo apt install apache2 -y
sudo apt install php libapache2-mod-php -y
cd /var/www/html
sudo rm index.html
sudo apt install curl
sudo curl -o replicator.php https://raw.githubusercontent.com/LafeLabs/sloth/main/php/replicator.txt
cd ..
sudo chmod -R 0777 *
cd html
php replicator.php
sudo chmod -R 0777 *
```

This will clone the trash web to your server. 

Now go into the DNS records of a domain you have access to or ask someone else to it for a domain they have access to and add an "A record" with entries "@" and "www" for that domain to the home IP address of wherever the server is located.  Set up port forwarding on ports 80 and 443 on the router for that local network.  Or have someone point a sub-domain to the server, like sloth.trashphysics.org for example.

To make a folder on the desktop in Ubuntu which maps to the html folder use

```
ln -s /var/www/html/sloths ~/Desktop/sloths
```

## TRASH ROBOT SOCIALS

 - [TIKTOK](https://tiktok.com/@trash_robot)
 - [INSTAGRAM](https://www.instagram.com/lafelabs/)
 - [MASTODON](https://kolektiva.social/@trashrobot)
 - [GITHUB](https://github.com/lafelabs)
 - [TRASHROBOT DOT ORG](https://trashrobot.org/)


