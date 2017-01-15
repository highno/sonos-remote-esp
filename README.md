# sonos-remote-esp
Code for a SONOS remote based on arduino and esp8266

## Introduction
This is my codebase for an ESP8266-12 arduino based SONOS Remote featuring an
OLED Display (SH1106-based) and 4 Buttons (Left, Right, Enter and Menu).
The idea behind this is, my SONOS speakers are connected to the TV set and volume
changes drastically whenever commercials pop up. I don't always have a mobile
device with me, and even if I do, it may take ages until you get to the SONOS app
and can finally reduce the volume.
This hardware (and the software) is still a learning project for me, so I can
live with it being a wired, not power optimized, remote at this time.
Power optimization, in addition to a switch to battery power and design of a
charging cradle (wireless!) is on my list - but on the later part... 

## Usage
The system so far does boot while giving a lot of info on the OLED. It looks
for a given hardcoded WiFi network but allows to switch over to a config mode
where the WiFiManager lib takes over and presents a config page via an open access
point. The new WiFi config is not yet stored in Flash, this is on my list.

The remote will then look for SONOS devices it can control. It will present all
devices found in a short list on the display and select the first one by default.
You can go into the menu and switch the controlled SONOS device by selecting
another device by its name.

You can change the volume of the connected SONOS device (which is shown on the
main screen) by using the left/right buttons and toggle pause/play via the enter
button. The menu is brought up by - you guessed it - the menu button.

## Idea
This ought to be a good learning project for me, trying to get used to arduino
in general and the ESP8266 in detail.
Please be gentle, I take the journey from the 'fat' side of live, the bigger x86
systems with lots of RAM and cpu cycles. I am used to using python to get my work
done, so my code does not yet look like it's made for microcontrollers. Also my
C/C++ skills have a lot of room for improvement.
If you like this project and/or have ideas of where to optimize the code, please
feel free to do so. I'd love to see how this will be turned into a more µC-like
code.
