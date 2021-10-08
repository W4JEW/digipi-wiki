# Welcome to the DigiPi Wiki

## Overview

### What is DigiPi?

An elegant, inexpensive, low-power, open-source Raspberry-Pi-Zero-based amateur radio digital interface, managed exclusively by web browsers or smart-phone apps, with no bulky keyboards, monitors or complicated wiring.

------

### Features & Functionality

- Packet Radio Terminal Node Controller
  - KISS Interface (via Wi-Fi or Bluetooth)
  - Use with xastir, yaac, woad, aprsdroid, and any open-standard KISS apps
- APRS Packet Radio Network Digipeater
  - Bridge APRS Network to the Internet
  - For email, SMS, and other online services...
- Winlink Server
  - Listen for Winlink radio clients requesting to send/recieve email
- Winlink Client
  - Pat - Web-based inbox/outbox email interface
  - ARDOP - Sound modem to connect to Winlink Servers around the globe over HF
  - Supports [WoAD](https://woad.sumusltd.com/) Android app - Connects to DigiPi wirelessly via TNC/KISS Interface (Wi-Fi or Bluetooth)
- AX.25 Networking
  - Radio connected network protocol used for Winlink/node services
  - IP Tunnel - legal Internet IP address on [AMPRnet](https://www.ampr.org/) (44.x.x.x/8 - Reserved for Ham Radio)
- Node Services
  - Run your own Bulletin Board Service (BBS) or messaging service
  - Connect to other nodes via intermediate nodes

------

### Building Blocks

DigiPi is a combination of hardware and software

Raspberry Pi Zero W (ideally with headers)

The Raspberry Pi 3 or 4 will not work with DigiPi. Plus, the Raspberry Pi Zero W consumes less power and has more than adequate system resources to support the feature set.

Audio Interface (GPIO-based) - RX and TX

PTT Interface - key the radio as needed

Visual Interface - combination of miniature TFT display and LEDs to provide visual indication of system status and activity

DigiPi image - pre-built image including Raspberry Pi OS, supporting applications, and recommended configuration settings