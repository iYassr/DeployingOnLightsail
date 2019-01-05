# DeployingOnLightsail


## Website info
IP: 13.233.62.118
SSH Port: 2200
URL: http://13.233.62.118.xip.io/

## Application Installed 

`sudo apt-get install apache2 libapache2-mod-wsgi-py3 pip3` 

## Configuration Changes and Security Hardeninig

| Change Made | Why |
| --- | --- |
| SSH Port from standard 22 to 2200 | Avoid scraping-bots and script kiddes - Security through obscurity - | 
| Allow incoming traffic only through 2200/SSH, 123/NTP/ 80/HTTP | Prevent hackers from exploiting unused ports | 
| Disable authantication through password | If we user public-key auth, why bother useing password that can be brue-forced |
| Run apache through www-data user | Running apache with unprivleged user makes hacker's life harder | 
| New user 'grader' and added to sudo group | Mr/Ms grader needs to grade |
| Keypair generated, public key added to ~.ssh/authorized_key | Mr/Ms grader needs to connect through ssh | 


## Resources 

http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi
https://coderwall.com/p/pstm1w/deploying-a-flask-app-at-heroku
https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps
