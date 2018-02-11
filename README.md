# elotouchxorg
Elo Touchscreen on RPi

After fiddling around for some hours I finally found a solution to get the Elo Touchscreen working correctly on my Raspberry Pi 3.
Depending on your screen you have to calibrate it and modify the values in the config and you maybe need to change the "MatchProduct" line.

For installation run sudo apt-get update, then sudo apt-get install xserver-xorg-input-evdev

Copy the 98-calibration.conf to /usr/share/X11/xorg.conf.d and reboot the RPi, done!
