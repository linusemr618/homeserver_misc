``` bash
apt update && apt upgrade
apt install cups printer-driver-hpcups avahi-daemon
systemctl enable --now cups avahi-daemon
adduser truenas_admin -u 950
adduser truenas_admin lpadmin
cupsctl --remote-any --remote-admin --share-printers
systemctl restart cups
# Add printer from https://printer:631
wget -O /etc/cups/ppd/HP_LaserJet_1100.ppd https://raw.githubusercontent.com/linusemr618/homeserver_misc/refs/heads/main/printer/HP_LaserJet_1100.ppd
#vim /etc/cups/ppd/HP_LaserJet_1100.ppd
systemctl restart cups
```
