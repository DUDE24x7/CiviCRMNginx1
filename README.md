# CCiviCRMNginx1

#create an AWS ubuntu 16.04 server
#Security group rules: SSH = port 20 (anywhere - normally I would set My Ip); HTTP = port 80 (anywhere); HTTPS = port 443 (anywhere)

#Copy the script below and run it after accessing the server from SSH

sudo apt-get update;
sudo apt-get install git;
git config --global user.name “Tom”;
git config --global user.email “judgemental1@me.com”;
git config --global core.editor nano;
mkdir gitdownload;
cd gitdownload;
git clone https://github.com/DUDE24x7/CiviCRMNginx1;
chmod 700 CiviCRMNginx1/AWS1.script;
cd;
echo "AWS1.script is starting";
gitdownload/CiviCRMNginx1/AWS1.script;
echo "AWS1.script has ended";

Afterwards setup Drupal from http://<your_home> and then
Install CiviCRM on Drupal from http://<your_drupal_home>/sites/all/modules/civicrm/install/index.php

Here are the sources of reference material for the task. The task requirement is documented below

NGINX MYSQL PHP
https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-in-ubuntu-16-04

Drupal 7.54
http://idroot.net/linux/install-drupal-ubuntu-16-04/

Configure NGINX for Drupal
http://blog.celogeek.com/201209/202/how-to-configure-nginx-php-fpm-drupal-7-0/
There was nothing to do here.

CiviCRM 4.7.19
Note – Default installation is a separate DB for CiviCRM and for Drupal
https://wiki.civicrm.org/confluence/display/CRMDOC/Installing+CiviCRM+for+Drupal+7

CiviCRM extensions https://wiki.civicrm.org/confluence/display/CRMDOC/Extensions#Extensions-Drupal

The requirement:
Drupal and CiviCRM 

Create a new server using Nginx on an AWS micro instance

Install Drupal 7 and CiviCRM this server in a secure fashion. You may wish to research what Nginx configurations are required to make both Drupal AND CiviCRM secure. Please install CiviCRM and Drupal in different databases as this is considered best practice. (this is the default)

1 Install Git to the server for the appropriate user (done)
2 Configure the CiviCRM extension directory correctly (done)
3 Ensure that the Nginx configuration is secure for CiviCRM (done)
