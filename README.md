# CCTask

#create an AWS ubuntu 16.04 server
# Security group rules: SSH = port 20 (My Ip); HTTP = port 80 (anywhere); HTTPS = port 443 (anywhere)

#Copy the script below and run it after accessing the server from SSH

sudo apt-get update;
sudo apt-get install git;
git config --global user.name “Tom”;
git config --global user.email “judgemental1@me.com”;
git config --global core.editor nano;
mkdir gitdownload;
cd gitdownload
git init;
git clone https://github.com/DUDE24x7/CCTask.git;
chmod 700 CCTask/AWS1.script;
cd;
echo "AWS1.script is starting";
gitdownload/CCTask/AWS1.script;
echo "AWS1.script has ended";

Afterwards setup Drupal from http://<your_home> and then
Install CiviCRM on Drupal from http://<your_drupal_home>/sites/all/modules/civicrm/install/index.php
