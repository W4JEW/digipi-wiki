# Shopping List

## Overview

If you are interested in building a DigiPi, it will require that you purchase several different components.



NOTE: *Save yourself a lot of time and headaches - please use the supported hardware. Do not make substitutions unless otherwise specified. If you do not see that it is safe to substitute, then it isn't. Stick with what's listed.*

The type of radio you intend to use can have a significant impact on the components that are required.

Your radio will likely fall into one of three categories:

1. Supports CAT Control and Audio via USB
2. Supports CAT Control via USB but not Audio via USB
3. Does NOT support CAT Control or Audio via USB

To make things a little easier to understand, instead of one shopping list with all of the possible options, there are three shopping lists - one for each type of radio. 

## Components

This is just a high-level overview of the components that make up the DigiPi solution.

### Raspberry Pi Zero W

- The brains and brawn of the operation - yes it does need to be a Zero W (ideally with pre-soldered headers)

- *Craig specifically states the Raspberry Pi 3B/3B+/4 will NOT work with DigiPi*

### Micro SD Card - 16 GB to 32 GB

You can safely buy a larger Micro SD Card, but 16 GB is more than sufficient

*Don't go the inexpensive route here! Buy a reputable brand.*

- Samsung Endurance are meant for use in demanding environments and are an excellent option!

- SanDisk Ultra or Extreme are also excellent options

- *Anything else - your mileage may vary! I have spoken!*

### GPIO Audio Interface

*OPTIONAL if radio includes integrated audio*

Two models have been tested:

1. Fe-Pi v2

2. Audio Interface Z

- Testing has proven that GPIO-based audio interfaces yield superior results to the inexpensive USB sound card dongles

- USB sound card dongles may have similar chipsets, but vary dramatically in terms of build quality and adherence to specifications, hence why it we strongly encourage you to avoid using them

- USB audio natively built into radios are an exception to this - they are very high quality and are not known exhibit the timing issues

### GPIO Stacking Header

- *OPTIONAL if your radio includes integrated audio*

- *MANDATORY if you need the GPIO audio interface*

- Solder to the GPIO audio interface

- The supported GPIO audio interfaces do not include headers - they must be added

- This provides connectivity to the Raspberry Pi Zero W and display

- Select a straight-through model (not angled) that has a 40-pin female connector on one side and 40-pin male connector on the other end

### PiTFT 1.3" Display

- Driven by  [Direwatch](https://github.com/craigerl/direwatch) written by none other than Craig - KM6LYW!

- Displays Direwolf/APRS/Packet activity on an Adafruit PiTFT display

- Default configuration is for the PiTFT 1.3" display (240x240 - ST7789)

- Direwatch also known to work with the Adafruit Mini-PiTFT Display (135x240) but the smaller display isn't very practical

### Field Effect Transistor (a.k.a. FET or MOSFET)

- MANDATORY if your radio does not support CAT control via USB

- Used to PTT your radio

- Don't be intimidated by the name - as Craig says *"Don't let the name fool you - it's just a switch"*

### Resistor - 100K 1/8W Resistor

- *MANDATORY* if your radio DOES NOT support CAT control via USB

- Also used to PTT your radio

### LEDs

*OPTIONAL but very nice to have*

- Provide visual indication of PTT activity and Bluetooth status

- Recommended colors Red (1x) Green (1x) Blue (1x)

### RJ-12 Cable

- *MANDATORY if your radio DOES NOT support CAT control via USB*

- Provides connectivity between DigiPi and your radio - ferrites recommended

- There's an alternative solution - see below

## Mobilinkd TNC Adapter

- *ALTERNATIVE to RJ-12 Cable*

- These are a great option as they allow you to use different radios interchangeably

- Simply purchase the Mobilinkd cable(s) for your radio directly from Mobilinkd `http://www.mobilinkd.com/`

### TRRS 3.5" Port

- *MANDATORY* if you opt for the Mobilinkd TNC cable

- Provides physical connectivity to the Raspberry Pi Zero W and GPIO audio interface

### USB to Micro USB Cable

*MANDATORY if your radio DOES support CAT Control and Audio via USB*

You already knew this, right?

### Micro USB On-the-Go Hub

Raspberry Pi Zero SBCs do allow you to connect USB devices but they must be connected via USB OTG (On-the-Go)

Just because it has a USB to Micro-USB adapter does not mean it will work

It **MUST** be USB OTG, otherwise, it will not work with a Raspberry Pi Zero

### Power Supply

Craig has yet to figure out wireless power - until then, you'll need a way to power the system.

- Ensure you select a power supply that provides *adequate* power to DigiPi.

- *Inadequate power introduces significant risk to the overall stability - you have been warned!*

- Recommended specifications 5.0/5.1 Volts & 2.5 Amps

- USB Buck adapters are a great option for use in the field - they allow you to use the same 12 V power supply for your radio

- AC Power for commercial power

## Specifics and Recommendations

### Raspberry Pi Zero W

- [MicroCenter - Raspberry Pi Zero WH - with Pre-Soldered Headers](https://www.microcenter.com/product/502843/raspberry-pi-zero-wh-with-pre-soldered-headers) - $13.99 USD

- [Adafruit - Raspberry Pi Zero WH (Zero W with Headers)](https://www.adafruit.com/product/3708) - $14.00 USD

### Micro SD Card - 16 GB to 32 GB

- [Samsung PRO Endurance 32GB 100MB/s (U1) MicroSDXC Memory Card - (MB-MJ32GA/AM)](https://www.amazon.com/Samsung-Endurance-128GB-Micro-Adapter/dp/B07B98GXQT/) - $9.99 USD

- [SanDisk Ultra 32GB UHS-I/Class 10 Micro SDHC Memory Card With Adapter - SDSDQUAN-032G-G4A](https://www.amazon.com/SanDisk-Ultra-UHS-I-Memory-Adapter/dp/B00M55C0NS/) - $8.37 USD

### GPIO Audio Interface

- [Fe-Pi v2: https://wb7fhc.com/order-nexus-now.html](https://wb7fhc.com/order-nexus-now.html) - $22.00 USD

*NOTE: The seller typically sells these with his Nexus DR-X Digital Radio Cross-Patch but he specifies that he will sell them separately (charges an additional fee).*

*Given the increased popularity of DigiPi, he has started to show apprehension about selling them separately. If he won't sell them to you, it's not the end of the world. Just go with the Audio Interface Z instead.*

- [Audio Interface Z](https://www.amazon.com/Audio-Injector-Zero-sound-Raspberry/dp/B075V1VNDD/) - $24.00 USD

### GPIO Stacking Header

- [GeeekPi 2x20 40 Pin Stacking Female Header Kit for Raspberry Pi 4B/3B+/3B/2B/B+/A+/Zero](https://www.amazon.com/gp/product/B08GC18NMK/) - $12.99 USD

- [Stacking Header for Pi A+/B+/Pi 2/Pi 3 - 2x20 Extra Tall Header](https://www.adafruit.com/product/1979/) - $2.99

### PiTFT 1.3" Display

- [Adafruit Mini PiTFT 1.3" - 240x240 TFT Add-on for Raspberry Pi](https://www.adafruit.com/product/4484) - $14.95 USD

- [DIYmall Mini PiTFT 1.3" LCD Display 240x240 TFT Add-on for Raspberry Pi 3.3V SPI ST7789 3.3V SPI ST7789 Full Color](https://www.amazon.com/gp/product/B08F9VD2GZ/) - $15.99 USD

*NOTE: This is a clone - it is not an official Adafruit PiTFT - but it does work!*

### Field Effect Transistor (a.k.a. FET or MOSFET)

- [Fairchild Semiconductor 2N7000 N Channel MOSFET, 60V, 200mA, TO-92](https://www.amazon.com/gp/product/B00M1GP3X0/) - $5.25 USD

### Resistor - 100K 1/8W Resistor

- [100 X Resistors 100K Ohms 0.125w 1/8w Cement 5% Tolerance](https://www.amazon.com/Resistors-100K-0-125w-Cement-Tolerance/dp/B07FNGV914/) - $3.99 USD

### LEDs

- [OFNMY LED Diode Lights, 3mm and 5mm LED Lights Emitting Diodes Assortment Set Kit](https://www.amazon.com/gp/product/B07STBXZDD/?th=1) - $9.99 USD

### RJ-12 Cable

- [NECABLES (2 Pack) RJ12 Cable 6ft Phone Cord RJ12 6P6C Male to Male Straight Wired 6-ft](https://www.amazon.com/gp/product/B08BHVF6XS/) - $6.99 USD

### Mobilinkd TNC Cable

- [Mobilinkd TNC Cables - Radio-specific](https://store.mobilinkd.com/collections/tnc-cables/) - Price varies (see website for details)

### TRRS 3.5" Port

- [Cylewet 3Pcs TRRS 3.5mm Stereo Audio Jack Breakout Board](https://www.amazon.com/gp/product/B01N7NDCVI/) - $7.69 USD

### USB to Micro USB Cable

- *Surely you have at least one of these laying around! :-)*

### Micro USB On-the-Go Hub

- [MakerSpot Micro USB OTG Hub for Raspberry Pi Zero 4 Port High Speed Sync and Extension Cable](https://www.amazon.com/gp/product/B01JL837X8/) - $6.99 USD

### Power Supply

- [Argon ONE Raspberry Pi Micro USB Cable Power Supply 5.25 Volts 3 Amps](https://www.amazon.com/Argon-Raspberry-Listed-Power-Supply/dp/B07MC7B9X3/) - $11.99 USD

*NOTE: These are AWESOME! They are the highest quality power supplies you can purchase for a Raspberry PI! Buy a few of them if you have other Raspberry Pis and throw out any of the others you're currently using. (Just a recommendation - don't take our word for it!)*

### Buck Converter

- [Buck Converter 12v to 5v, DROK 5A USB Voltage Regulator](https://www.amazon.com/Converter-DROK-Regulator-Inverter-Transformer/dp/B01NALDSJ0/) - $9.99
