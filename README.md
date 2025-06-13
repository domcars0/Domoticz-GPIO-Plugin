# Domoticz-GPIO-Plugin

Controls GPIO pins on a Raspberry Pi.

## Key Features

* Creates one Domoticz device per relay on GPIO pins.

## Installation

Python version 3.4 or higher required & Domoticz version 3.7xxx or greater.

To install:
* Run ```sudo pip3 install RPi.GPIO```
* Go in your Domoticz directory, open the plugins directory.
* Navigate to the directory using a command line
* Run: ```git clone https://github.com/domcars0/Domoticz-GPIO-Plugin.git```
* Restart Domoticz.

In the web UI, navigate to the Hardware page.  In the hardware dropdown there will be an entry called "Raspberry Pi GPIO".
* Allow New Hardware Devices in the Setup=>Settings=>System Page
* Add a new Hardware with this type (Raspberry Pi GPIO) and setup your gpio configuration. Click 'Add'
* This will create the new(s) device(s)
* Go to the Setup=>Devices. You will be able to see the new (not used) devices and can add them to the Switches Page.

That's all!

## Updating

To update:
* Go in your Domoticz directory using a command line and open the plugins directory then the Domoticz-GPIO-Plugin directory.
* Run: ```git pull```
* Restart Domoticz.

## Configuration

| Field | Information|
| ----- | ---------- |
| Output Pins | Comma delimited list of output (relay) pins. Format is pin number colon NO or NC or TO colon 0 or 1 (e.g 16:TO:1 will create an On/Off Button (TO), active_low (1) on GPIO pin 16 (GPIO23 on a Pi3B ) |
| Input Pins | Comma delimited list of board pin numbers (1-40) to check for input |
| Switch Debounce | Time (ms) between valid switch presses, prevents multi reports of events |
| Heartbeat Frequency | Determines how often Input Pins are checked for values |
| Debug | When true the logging level will be much higher to aid with troubleshooting |

Notes : If you want to change the Type of an output button created by the plugin use the Device setup button (change it in the plugin will do nothing).
Notes 2: To remove a device remove his pin number in the comma separated list of inputs or ouputs. Cause if you remove it via the DZ Switches page, the plugin will recreate it on the next start.

## Change log

| Version | Information|
| ----- | ---------- |
| 1.0.0 | Initial upload version |
| 2.0.0 | Can now create Output types : On/Off Button (TO), Push Off Button (NC) or Push On Button (NO), active_low (1) or active_high (0) |
