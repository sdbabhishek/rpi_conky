# rpi_conky

1. adding conky to raspberry pi

sudo apt-get install conky


2. download the conkyrc file to home directory as .conkyrc

wget -O /home/pi/.conkyrc https://github.com/sdbabhishek/rpi_conky/blob/master/rpi3_conkyrc


3. create the shell script

sudo nano /usr/bin/conky.sh


4. paste this into the conky.sh file

#!/bin/sh
(sleep 4s && conky) &
exit 0


5. now lets create the conky.desktop file for the autostart process

sudo nano /etc/xdg/autostart/conky.desktop


6. and paste this into the file

[Desktop Entry]
Name=conky
Type=Application
Exec=sh /usr/bin/conky.sh
Terminal=false
Comment=system monitoring tool.
Categories=Utility;



7. the last thing to do is to reboot to make sure everything is working!
