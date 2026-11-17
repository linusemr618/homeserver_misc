``` bash
apt update
apt upgrade
apt install cups printer-driver-hpcups avahi-daemon
adduser truenas_admin -u 950
adduser truenas_admin lpadmin
cupsctl --remote-any --remote-admin --share-printers
service cups restart
# Add printer from https://printer:631
vim /etc/cups/ppd/HP_LaserJet_1100.ppd
service cups restart
```
