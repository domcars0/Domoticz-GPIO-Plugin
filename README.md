# Domoticz-GPIO-Plugin

Controls GPIO pins on a Raspberry Pi.

## Key Features

* Creates one Domoticz device per relay.

## Installation

Python version 3.4 or higher required & Domoticz version 3.7xxx or greater.

To install:
* Run ```sudo pip3 install RPi.GPIO```
* Go in your Domoticz directory, open the plugins directory.
* Navigate to the directory using a command line
* Run: ```git clone https://github.com/dnpwwo/Domoticz-GPIO-Plugin.git```
* Restart Domoticz.

In the web UI, navigate to the Hardware page.  In the hardware dropdown there will be an entry called "Raspberry Pi GPIO".

## Updating

To update:
* Go in your Domoticz directory using a command line and open the plugins directory then the Domoticz-GPIO-Plugin directory.
* Run: ```git pull```
* Restart Domoticz.

## Configuration

| Field | Information|
| ----- | ---------- |
| Output Pins | Comma delimited list of output (relay) pins. Format is pin number colon NO or NC (e.g 39:NO) |
| Input Pins | Comma delimited list of board pin numbers (1-40) to check for input |
| Switch Debounce | Time (ms) between valid switch presses, prevents multi reports of events |
| Heartbeat Frequency | Determines how often Input Pins are checked for values |
| Debug | When true the logging level will be much higher to aid with troubleshooting |

## Change log

| Version | Information|
| ----- | ---------- |
| 1.0.0 | Initial upload version |
