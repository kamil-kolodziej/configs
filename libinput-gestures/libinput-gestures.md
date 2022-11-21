libinput-gestures
https://github.com/bulletmark/libinput-gestures



sudo gpasswd -a $USER input

sudo apt-get install wmctrl xdotool

sudo apt-get install libinput-tools

git clone https://github.com/bulletmark/libinput-gestures.git
cd libinput-gestures
sudo make install (or sudo ./libinput-gestures-setup install)

Autostart On:
libinput-gestures-setup autostart start

To test:
# Ensure the program is stopped
libinput-gestures-setup stop
# Test to print out commands that would be executed:
libinput-gestures -d
(<ctrl-c> to stop)

The default gestures are in /etc/libinput-gestures.conf. If you want to create your own custom gestures then copy that file to ~/.config/libinput-gestures.conf and edit it. There are many examples and options described in that file.

config file:
comment out: gesture swipe up	_internal ws_up
uncomment:
gesture pinch in	xdotool key ctrl+F9
gesture pinch out	xdotool key ctrl+F9

add:
gesture swipe left		_internal --cols 4 ws_right
gesture swipe right		_internal --cols 4 ws_left
gesture swipe up	    xdotool key ctrl+F8
gesture swipe down	  xdotool key ctrl+F8
