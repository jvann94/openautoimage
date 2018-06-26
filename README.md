# OpenAuto Image

### NOTE THIS IS FOR A FULL FLEDGED CAR-PUTER USE AT YOUR OWN RISK, I AM NOT RESPONSIBLE FOR ANY INJURY YOU BRING YOURSELF OR OTHERS WHEN USING THIS TOOL

My custom Image with OpenAuto pre-compiled for a raspberry pi 3. This allows you to have a sudo plug and play experience with running android auto on a raspberry pi.

This image uses Raspbian as a base and has f1xpl's android auto head unit emulator software installed on it (https://github.com/f1xpl/openauto). He has the build instructions list on his wiki for building from scratch. The backlight on screen is controlled with rpi-backlight (https://github.com/linusg/rpi-backlight).

On top of those I have added desktop short cuts to launch OpenAuto and to dim and increase the brightness of the official Pi screen

# Future features

### Bluetooth

Currently there is a problem with raspbian playing audio over bluetooth. the speaker pairs and connects. pulse recognizes it as an audio device and plays to it but no audio comes from the speaker.

### Backup camera

  To add a backup camera to the system it would consist of a cheap NTSC camera that the pi switched to when it seas the reverse rights come one. it would watch a GPIO pin and wait for it to go high and then run the command to open the feed from a USB capture card.
 
### OBDII support

I need to figure out how to make my cheap ELM 327 bluetooth OBDII reader talk to the scantool software and it was making me pull my hair out a little bit.

### Buttons

I'd Like to install a few hardware buttons to perform certain functions. perhaps one to act as an alt-tab function to switch between openauto, scantool, and any other active window.

Another button could be a stepped screen brightness system to manually adjust the screen brightness as apposed to a light sensor controlling the brightness.
