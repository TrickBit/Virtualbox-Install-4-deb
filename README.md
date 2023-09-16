# Virtualbox-Install-4-deb
Script to install VirtualBox based on info from https://www.virtualbox.org/wiki/Linux_Downloads

Pretty simple script!

Follows the instructions at https://www.virtualbox.org/wiki/Linux_Downloads

Debian-based Linux distributions
Add the following line to your /etc/apt/sources.list. For Debian 11 and older, replace '<mydist>' with 'bullseye', 'buster', or 'stretch'. For Ubuntu 22.04 and older, 'replace '<mydist>' with 'jammy', 'eoan', 'bionic', 'xenial',

deb [arch=amd64 signed-by=/usr/share/keyrings/oracle-virtualbox-2016.gpg] https://download.virtualbox.org/virtualbox/debian <mydist> contrib
The Oracle public key for verifying the signatures can be downloaded here. You can add these keys with

sudo gpg --dearmor oracle_vbox_2016.asc --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg
or combine downloading and registering:

wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg

The key fingerprint for oracle_vbox_2016.asc is

B9F8 D658 297A F3EF C18D  5CDF A2F6 83C5 2980 AECF
Oracle Corporation (VirtualBox archive signing key) <info@virtualbox.org>
To install VirtualBox, do

sudo apt-get update
sudo apt-get install virtualbox-6.1  

Note the version as of writing for Ubuntu 22.04 are 6.1 and 7.0
