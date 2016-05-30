# udacityfullstack_p5_linux_server_configuration

IP Address: 52.11.96.19 <br>
SSH Port: 2200 <br>
URL: http://ec2-52-11-96-19.us-west-2.compute.amazonaws.com/login <br>

### Login Instructions

Click on the URL link above
Hit the Login button and sign-on with G+ account
![Login Button](/login.png?raw=true "login")


### Software Installed
pip install dict2xml
pip install Flask
pip install Flask-SQLAlchemy
pip install httplib2
pip install psycopg2
pip install requests
pip install sqlalchemy
sudo apt-get install apache2
sudo apt-get install dict2xml
sudo apt-get install git
sudo apt-get install libapache2-mod-wsgi python-dev
sudo apt-get install pip
sudo apt-get install postgresql postgresql-contrib
sudo apt-get install postgresql-server
sudo apt-get install python-pip
sudo apt-get install python-psycopg2
sudo apt-get install python-setuptools libapache2-mod-wsgi
sudo easy_install pip
sudo pip install --upgrade oauth2client
sudo pip install dict2xml
sudo pip install Flask
sudo pip install Flask-Login==0.1.3
sudo pip install flask-seasurf
sudo pip install flask==0.9
sudo pip install sqlalchemy
sudo pip install virtualenv
sudo pip install werkzeug==0.8.3

### Configuration Changes Made
## User Management
- create new user grader with sudo permissions (password provided in review submission to Udacity reviewer)
- sudo commands prompt for user password at least once.
- Remote login of the root user has been disabled.
- A remote user is given sudo access.
- Users have good/secure passwords.

## Security
- Configure the local timezone to UTC
- Only allow connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
- Key-based SSH authentication is enforced.
- Applications have been updated to most recent updates.
- SSH is hosted on non-default port.

## Application Functionality
- Database server has been configured to serve data (postresql is recommended).
- VM can be remotely logged into.??
- Web-server has been configured to serve the Item Catalog application as a wsgi app.
- Made minor changes to app (primary key constraint, changed filenames to save photos, adjusted permissions as well in order to allow users ot upload files to the server)
- Got Google+ oauth working

### Third Party Resources
- Very useful step-by-step guide: https://github.com/stueken/FSND-P5_Linux-Server-Configuration
- DigitalOcean.com
- Stackoverflow for adjusting permissions to allow file uploads
- Apache Enabling and disabling sites: http://snipplr.com/view/15626/apache2--enabling-and-disabling-sites/
- Permissions for users to upload files: http://askubuntu.com/questions/196062/sftp-permission-denied-on-files-owned-by-www-data ; https://wiki.apache.org/httpd/13PermissionDenied
- Permissions/User Mgmt: https://serversforhackers.com/permissions-and-user-management
- Reboot after adjusting groups: http://serverfault.com/questions/98900/is-a-reboot-required-to-refresh-permissions-after-adding-a-user-to-a-new-group

### Useful Commands
- Logging in: ssh -i ~/Downloads/udacity_key.rsa grader@52.11.96.19 -p2200 (note insecure key)
- psql: sudo -u postgres psql
- restarting/reloading apache2: sudo service apache2 restart ; service apache2 reload
- remove root passwd: sudo passwd -l root
- restart ssh: sudo service ssh restart
- login as root sudo -i
- adjust config: sudo nano /etc/ssh/sshd_config

### ~/.ssh/udacity_key.rsa
- contents submitted in the "Notes to Reviewer"

