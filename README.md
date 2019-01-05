# DeployingOnLightsail


## Website info
IP: 13.233.62.118
SSH Port: 2200
URL: http://13.233.62.118.xip.io/



## Application Installed 

`sudo apt-get install apache2 libapache2-mod-wsgi-py3` 


## Configuration changes and Security Hardeninig

| change Made | Why |
| SSH Port from standard 22 to 2200 | avoid scraping-bots and script kiddes - Security through obscurity - | 
| allow incoming traffic only through 2200/SSH, 123/NTP/ 80/HTTP | prevent hackers from exploiting unused ports | 
| run apache through www-data user | running apache with unprivleged user makes hacker's life harder | 
| new user 'grader' and added to sudo group | Mr/Ms grader needs to grade |
| keypair generated, public key added to ~.ssh/authorized_key | Mr/Ms grader needs to connect through ssh | 


## Resources 

http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/




i. The IP address and SSH port so your server can be accessed by the reviewer.
ii. The complete URL to your hosted web application.
iii. A summary of software you installed and configuration changes made.
iv. A list of any third-party resources you made use of to complete this project.

Locate the SSH key you created for the grader user.

During the submission process, paste the contents of the grader user's SSH key into the "Notes to Reviewer" field.
