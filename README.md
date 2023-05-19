# 6502 Based Personal Computer
### Warnings!:
This is my first time designing a 4-layer PCB, and my first time designing a computer,
also I did not order the PCB so I don't know if it works, don't hold me responsible.

This contains surface mount compunents!! if you're not skilled with soldering I recommend paying for an assembly service.
### 3D View:
#### Top:
![image](https://github.com/ChromiumOS-Guy/6502PC/assets/57168079/98b340f3-616f-410b-b250-78c003d1ed4a)
#### Buttom:
![image](https://github.com/ChromiumOS-Guy/6502PC/assets/57168079/cc954a61-e98a-4b84-ae67-ba8786aa9903)
### Specs chart:
NAME | PART NUMBER | Datasheet
------------- | ------------- | -------------
CPU(10Mhz) | W65C02S6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C02S6TPG-14.pdf
RAM(16Kb) | AS6C62256-55PCN | https://componentsearchengine.com/Datasheets/1/AS6C62256-55PCN.pdf
VIA(IO) | W65C22S6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C22S6TPG-14.pdf
ACIA(UART) | W65C51N6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C51N6TPG-14.pdf
ROM(32Kb) | AT28C256-15PU | https://www.mouser.com/datasheet/2/268/doc0006-1108095.pdf
### Address Table:
PART NUMBER | BINARY-ADDRESS | HEX-ADDRESS | REGISTER SELECT
------------- | ------------- | ------------- | -------------
AS6C62256-55PCN(RAM) | 00(XXXXXXXXXXXXXX) | 0x0000-0x3FFF | A0-14(not fully used)
USER(Socket near CPU for adding new IC) | 0100XXXXXXXXXXXX | 0x4000-0x4FFF | Depends on IC plugged.
W65C22S6TPG-14(VIA) | 0101XXXXXXXX(XXXX) | 0x5000-0x5FFF | RS0-3 = A0-3
W65C22S6TPG-14(VIA) | 0110XXXXXXXX(XXXX) | 0x6000-0x6FFF | RS0-3 = A0-3
W65C51N6TPG-14(ACIA) | 0111XXXXXXXXXX(XX) | 0x7000-0x7FFF | RS0-1 = A0-1
AT28C256-15PU(ROM) | 1(XXXXXXXXXXXXXXX) | 0x8000-0xFFFF | A0-14
### TIPS:
If you're going to make this I strongly recommend reading at least the schematic,
also you'll need to buy the ROM (AT28C256-15PU) separately if you're using an assembly service.
Don't forget to buy an EPROM programmer that supports this specific EPROM if you don't already have one,
also don't forget to buy a USB to RS232 Interface Adapter if you don't already have one (optional but highly recommended)
