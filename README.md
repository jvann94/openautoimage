# OpenAuto Image

### NOTE THIS IS FOR A FULL FLEDGED CAR-PUTER USE AT YOUR OWN RISK, I AM NOT RESPONSIBLE FOR ANY INJURY YOU BRING YOURSELF OR OTHERS WHEN USING THIS TOOL

## I plan on releasing a smaller image soon based on the latest raspbian with the button software set up.

My custom Image with OpenAuto pre-compiled for a raspberry pi 3. This allows you to have a sudo plug and play experience with running android auto on a raspberry pi.

This image uses Raspbian as a base and has f1xpl's android auto head unit emulator software installed on it (https://github.com/f1xpl/openauto). He has the build instructions list on his wiki for building from scratch. The backlight on screen is controlled with rpi-backlight (https://github.com/linusg/rpi-backlight).

On top of those I have added desktop short cuts to launch OpenAuto and to dim and increase the brightness of the official Pi

### Screen brightness

Screen brightness can now be controlled via 2 external buttons wired into GPIO pins 22 and 27. This uses gpio-watch (https://github.com/larsks/gpio-watch) to monitor those pins to go high then runs the appririate bash script to set the back light to high or low.

# Future features

### Bluetooth

Currently expiriencing a problem with raspbian playing audio over bluetooth. the speaker pairs and connects. pulse recognizes it as an audio device and plays to it but no audio comes from the speaker.

### Backup camera

  To add a backup camera to the system it would consist of a cheap NTSC camera that the pi switched to when it sees the reverse rights come one. it would watch a GPIO pin and wait for it to go high and then run the command to open the feed from a USB capture card.
 
### OBDII support

I need to figure out how to make my cheap ELM 327 bluetooth OBDII reader talk to the scantool software. scantool no longer supports chinese knockoff readers and will force close when it sees youre using one of these. A work around is needed.

### Buttons

I'd Like to install a few hardware buttons to perform certain functions. perhaps one to act as an alt-tab function to switch between openauto, scantool, and any other active window. This is still in testing, the plan is to use GPIO-WATCH by larsks to watch gpio pins 22 and 27. to get gpio watch to run yoou need to echo the pin numbers in the pin export to get the pi to see the pins.
