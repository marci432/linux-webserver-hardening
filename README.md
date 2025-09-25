# linux-webserver-hardening
This project demonstrates how to set up and use an Apache web server on Ubuntu.  
The configuration is done through a VirtualHost, which serves files from a specific directory on the server.  

There are two main scripts included:  

1. setup.sh  
   - Creates a dedicated user for managing the web files.  
   - Installs and configures Apache.  
   - Sets up a VirtualHost for the website.  
   - Creates a simple test page.  
   - Enables basic security with UFW and Fail2ban.  
   This script only needs to be run once to prepare the environment.  

2. deploy.sh  
   - Synchronizes the contents of the local "site" folder with the server’s web directory.  
   - Ensures correct file ownership and permissions.  
   - Reloads Apache to apply changes.  
   This script can be run every time the website content needs to be updated.  

In short, `setup.sh` prepares the server, and `deploy.sh` makes it easy to deploy or update your website files.  
