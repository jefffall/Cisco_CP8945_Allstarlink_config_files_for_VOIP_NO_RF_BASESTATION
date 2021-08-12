The conf.xml file msut have the MAC address of your CP8945 as the file name to be picked up from tftp

put the file in your tftp directory:

for example:

/srv/tftp

#######################################
Here is the contents of the tftp file:

#root@pi1:/etc/default# more tftpd-hpa
TFTP_USERNAME="tftp"
TFTP_DIRECTORY="/srv/tftp"
TFTP_ADDRESS="192.168.1.58:69"
TFTP_OPTIONS="--ipv4 --secure -vvv"
######################################
here is the tftp server:

ii  tftpd-hpa                          5.2+20150808-1                      armhf        HPA's tftp server

Install it with

apt-get install tftpd-hpa

root@pi1:/etc/default# apt-get install tftpd-hpa
Reading package lists... Done
Building dependency tree
Reading state information... Done
tftpd-hpa is already the newest version (5.2+20150808-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.


First try to edit /etc/default/tftpd-hpa and try to get the lines to match as above and set to your IP address
of your PI or Ubuntu server.

Make sure you copy tftpd-hpa to /etc/default on a Pi or Ubuntu

You will set the IP of your PI or Ubuntu server in the phone. The "Active Server" listed on the phone info is the tftp server in SIP firmware load.

See the jpg pictures on how to set up your phone.
Look at the address in the XML file for the phone in this directory. Set the IP's to match your network.
Set up the phone to those IP's using the GEAR settings button and the JPG photos here.
