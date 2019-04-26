# Udacity_server_project

My catalog project is running on the IP address 54.185.143.107. The URL to my application is http://54.185.143.107/, and the ssh port is 2200. 

## Software I installed:
* Apache2
* Python3
* Python3 libraries used by my application (Flask, Sqlalchemy, and Oauth2client)
* Mod_wsgi for Python3
* Sqlite3
* Postgresql
* Git

## Summary of changes I made:
### I made the following changes to set up and secure my server:
* Updated all currently installed packages
* Configured the Amazon Lightsail firewall to allow SSH connections from port 2200
* Changed the SSH port to 2200
* Edited the SSH configuration file to not allow remote root user login
* Configured the UFW firewall to allow only connections from  ports 2200, 80, and 123
* Created a new user named grader with permission to sudo
* Created a ssh key pair for grader
* Created a database user "catalog" with permissions on the catalog application database
* Verified that my postgresql configuration file does not allow remote connections

### I made the following changes to serve my Python application over mod_wsgi:
* Cloned my Python application from GitHub
* Created a .wsgi file to load the application
* Created and enabled an Apache configuration file to serve my application
* Disabled the default Apache configuration file

## Resources I used:
In addition to the materials provided by Udacity, I also utilized the following third-party tutorials:
* https://umar-yusuf.blogspot.com/2018/02/deploying-python-flask-web-app-on.html
* https://tableplus.io/blog/2018/04/postgresql-how-to-grant-access-to-users.html
* http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/
* https://www.jakowicz.com/flask-apache-wsgi/
* https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps
