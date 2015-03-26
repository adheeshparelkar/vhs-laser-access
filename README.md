# Laser Access Controller

Used to automate the startup and shutdown of the laser cutter and all of the dependant devices from a Raspberry Pi

It is also used to control access to the laser. Access is handled by the membership management application.

## Wiring

* Chiller Relay - GPIO17, pin 11
* Ventilation Relay - GPIO27 pin 13
* Laser Relay - GPIO22 pin 15
* Main On/Off Switch - GPIO4 pin 7
* Green LED - GPIO23 pin 16
* Red LED - GPIO24 pin 18

The following pins are used for NFC but it's currently not enabled.

* Buzzer - GPIO18 pin 12
* NFC Reset GPIO25 pin 22
* NFC MOSI GPIO10 pin 19
* NFC MOSO GPIO09 pin 21
* NFC CLK GPIO11 pin 23
* NFC CE0 GPIO08 pin 24
* NFC CE1 GPIO07 pin 26

## Installation

After node.js is installed from the root of the project run:

    npm install

When installing on the production device you don't need to install the dev dependencies.

    npm install --production

Installing on a RPi does take a while.

## Config

Start by adding a new config.json file, see config.json.sample for an example.

## Testing

If dev dependencies are installed

    npm test

## Running

To set the port set the environment variable PORT to whatever port you want to listen to, by default it's 3000

    npm start

To enable debug logging then set the environment variable DEBUG to laser:* to log all laser related events.