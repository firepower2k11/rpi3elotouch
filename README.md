# rpi3elotouch
## Elo Touchscreen on RPi

After fiddling around for some hours I finally found a solution to get the Elo Touchscreen working correctly on my Raspberry Pi 3.
Depending on your screen you have to calibrate it, modify the values in the config and you maybe need to change the "MatchProduct" line depending on your touchscreen.

For installation run
```
sudo apt-get update
sudo apt-get install xserver-xorg-input-evdev
```

Copy the 98-calibration.conf to /usr/share/X11/xorg.conf.d and reboot the RPi, done!

For a good virtual keyboard run
```
sudo apt-get install at-spi2-core florence
```
and reboot the RPi.


### Getting Product ID for "MatchProduct"

Run
```
lsusb
```
in terminal and look for the line containing "Elo TouchSystems (...)", copy the full name and replace it on the "MatchProduct" parameter.
