# 6502 Based Personal Computer
### Warnings!:
This is my first time designing a 4-layer PCB, and my first time designing a computer,
also I did not order the PCB so I don't know if it works, don't hold me responsible
### Specs chart:
NAME | PART NUMBER | Datasheet
------------- | ------------- | -------------
CPU | W65C02S6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C02S6TPG-14.pdf
RAM | AS6C62256-55PCN | https://componentsearchengine.com/Datasheets/1/AS6C62256-55PCN.pdf
VIA | W65C22S6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C22S6TPG-14.pdf
ACIA | W65C51N6TPG-14 | https://componentsearchengine.com/Datasheets/1/W65C51N6TPG-14.pdf
ROM | AT28C256-15PU | https://www.mouser.com/datasheet/2/268/doc0006-1108095.pdf
### Address Table:
PART NUMBER | BINARY-ADDRESS | HEX-ADDRESS | ADDRESS&CONTROL
------------- | ------------- | ------------- | -------------
AS6C62256-55PCN(RAM) | 00(XXXXXXXXXXXXXX) | 0x0000-0x3FFF | A0-14(not fully used)
USER(Socket near CPU for adding new IC) | 0100(XXXXXXXXXXXX) | 0x4000-0x4FFF | Unknown
W65C22S6TPG-14(VIA) | 0101XXXXXXXX(XXXX) | 0x5000-0x5FFF | RS0-3 = A0-3
W65C22S6TPG-14(VIA) | 0110XXXXXXXX(XXXX) | 0x6000-0x6FFF | RS0-3 = A0-3
W65C51N6TPG-14(ACIA) | 0111XXXXXXXXXX(XX) | 0x7000-0x7FFF | RS0-1 = A0-1
AT28C256-15PU(ROM) | 1(XXXXXXXXXXXXXXX) | 0x8000-0xFFFF | A0-14
