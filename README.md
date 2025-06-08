# micro CAN Bus
[![GitHub stars](https://badgen.net/github/stars/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/stargazers/)
[![GitHub forks](https://badgen.net/github/forks/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/network/)
[![GitHub watchers](https://badgen.net/github/watchers/iDoka/awesome-canbus/)](https://GitHub.com/iDoka/awesome-canbus/watchers/)
[![GitHub contributors](https://badgen.net/github/contributors/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/graphs/contributors/)
[![GitHub pull-requests merged](https://badgen.net/github/merged-prs/iDoka/awesome-canbus)](https://github.com/iDoka/awesome-canbus/pulls?q=is%3Amerged)
[![GitHub latest commit](https://badgen.net/github/last-commit/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/commit/)

<p align="center"><img src="https://github.com/iDoka/awesome-canbus/raw/main/media/can_logo.png" alt="CAN logo"/></p>

<!--<p align="center">
<img src="https://github.com/iDoka/awesome-canbus/raw/main/media/can_logo.png" alt="CAN logo"/>
</p>-->

<!-- # :tractor: Awesome Tools, Hardware and Resources for CAN Bus 
[![GitHub latest commit](https://badgen.net/github/last-commit/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/commit/)
[![GitHub forks](https://badgen.net/github/forks/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/network/)
[![GitHub stars](https://badgen.net/github/stars/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/stargazers/)
[![GitHub watchers](https://badgen.net/github/watchers/iDoka/awesome-canbus/)](https://GitHub.com/iDoka/awesome-canbus/watchers/)
[![GitHub contributors](https://img.shields.io/github/contributors/iDoka/badges.svg)](https://GitHub.com/iDoka/badges/graphs/contributors/)
[![GitHub contributors](https://badgen.net/github/contributors/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/graphs/contributors/)
[![PR welcome issues still open](https://badgen.net/https/pr-welcome-badge.vercel.app/api/badge/fastify/help)](https://github.com/iDoka/awesome-canbus/)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/iDoka/awesome-canbus.svg)](https://GitHub.com/iDoka/awesome-canbus/pull/)
[![GitHub pull-requests merged](https://badgen.net/github/merged-prs/iDoka/awesome-canbus)](https://github.com/iDoka/awesome-canbus/pulls?q=is%3Amerged)
[![GitHub latest commit](https://badgen.net/github/last-commit/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/commit/)
-->


> :tractor: Awesome Tools, Hardware And Resources For CAN Bus

This curated list helps a reverse engineering CAN bus devices with lightly specializing in automotive embedded controller software and communication understanding.

> **Note**
> Items marked as "🔝" are highly recommended.








# Arduino CAN

[![Build Status](https://travis-ci.org/sandeepmistry/arduino-CAN.svg?branch=master)](https://travis-ci.org/sandeepmistry/arduino-CAN)

An Arduino library for sending and receiving data using CAN bus.

## Compatible Hardware

* [Microchip MCP2515](http://www.microchip.com/wwwproducts/en/en010406) based boards/shields
  * [Arduino MKR CAN shield](https://store.arduino.cc/arduino-mkr-can-shield)
* [Espressif ESP32](http://espressif.com/en/products/hardware/esp32/overview)'s built-in [SJA1000](https://www.nxp.com/products/analog/interfaces/in-vehicle-network/can-transceiver-and-controllers/stand-alone-can-controller:SJA1000T) compatible CAN controller with an external 3.3V CAN transceiver

### Microchip MCP2515 wiring

| Microchip MCP2515 | Arduino |
| :---------------: | :-----: |
| VCC | 5V |
| GND | GND |
| SCK | SCK |
| SO | MISO |
| SI | MOSI |
| CS | 10 |
| INT | 2 |


`CS` and `INT` pins can be changed by using `CAN.setPins(cs, irq)`. `INT` pin is optional, it is only needed for receive callback mode. If `INT` pin is used, it **must** be interrupt capable via [`attachInterrupt(...)`](https://www.arduino.cc/reference/en/language/functions/external-interrupts/attachinterrupt/).

**NOTE**: Logic level converters must be used for boards which operate at 3.3V.

### Espressif ESP32 wiring

Requires an external 3.3V CAN transceiver, such as a [TI SN65HVD230](http://www.ti.com/product/SN65HVD230).

| CAN transceiver | ESP32 |
| :-------------: | :---: |
| 3V3 | 3V3 |
| GND | GND |
| CTX | GPIO_5 |
| CRX | GPIO_4 |

`CTX` and `CRX` pins can be changed by using `CAN.setPins(rx, tx)`.

## Installation

### Using the Arduino IDE Library Manager

1. Choose `Sketch` -> `Include Library` -> `Manage Libraries...`
2. Type `CAN` into the search box.
3. Click the row to select the library.
4. Click the `Install` button to install the library.

### Using Git

```sh
cd ~/Documents/Arduino/libraries/
git clone https://github.com/yasir-shahzad/uCANPack
```

## API

See [API.md](API.md).

## Examples

See [examples](examples) folder.

For OBD-II examples, checkout the [arduino-OBD2](https://github.com/Yasir-Shahzad/arduino-OBD2) library's [examples](https://github.com/Yasir-shahzad/arduino-OBD2/examples).

## License

This library is [licensed](LICENSE) under the [MIT Licence](http://en.wikipedia.org/wiki/MIT_License).




# Arduino CAN Bus [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://badgen.net/github/stars/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/stargazers/)
[![GitHub forks](https://badgen.net/github/forks/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/network/)
[![GitHub watchers](https://badgen.net/github/watchers/iDoka/awesome-canbus/)](https://GitHub.com/iDoka/awesome-canbus/watchers/)
[![GitHub contributors](https://badgen.net/github/contributors/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/graphs/contributors/)
[![GitHub pull-requests merged](https://badgen.net/github/merged-prs/iDoka/awesome-canbus)](https://github.com/iDoka/awesome-canbus/pulls?q=is%3Amerged)
[![GitHub latest commit](https://badgen.net/github/last-commit/iDoka/awesome-canbus)](https://GitHub.com/iDoka/awesome-canbus/commit/)

<p align="center"><img src="https://github.com/iDoka/awesome-canbus/raw/main/media/can_logo.png" alt="CAN logo"/></p>

> :hammer_and_wrench: Awesome Tools, Hardware, and Resources for Arduino CAN Bus

This curated list focuses on tools, hardware, and resources for working with the CAN (Controller Area Network) bus using Arduino, with a special emphasis on automotive embedded controller software and communication projects.

> **Note**
> Items marked as "🔝" are highly recommended.

Permanent URL to this list: https://github.com/iDoka/awesome-canbus

## Contents

* [Hacking and Reverse Engineering Tools](#hacking-and-reverse-engineering-tools)
* [Test Equipment and Simulators](#test-equipment-and-simulators)
* [Protocols](#protocols)
  * [OBD-II Tools](#obd-ii-tools)
  * [J1939 Tools](#j1939-tools)
* [Utils](#utils)
  * [Common](#common)
  * [Arduino-Specific](#arduino-specific)
  * [Libraries](#libraries)
  * [Examples](#examples)
* [CAN Database](#can-database)
  * [Formats (DBC, KCD)](#formats-dbc-kcd)
  * [Converters and Parsers](#converters-and-parsers)
  * [DBC Only](#dbc-only)
* [Hardware](#hardware)
  * [Arduino](#arduino)
  * [Hardware-Related Tools](#hardware-related-tools)

## Hacking and Reverse Engineering Tools

* 🔝[Caring Caribou](https://github.com/CaringCaribou/caringcaribou) - A friendly car security exploration tool for the CAN bus, compatible with Arduino setups.
* 🔝[CAN_Reverse_Engineering](https://github.com/brent-stone/CAN_Reverse_Engineering) - Automated payload reverse engineering pipeline for CAN, adaptable for Arduino projects.
* [parse_can_logs](https://github.com/v-ivanyshyn/parse_can_logs) - Parse CAN logs and visualize data streams, usable with Arduino data.
* [canDrive](https://github.com/adamtheone/canDrive) - Tools for hacking your car, with Arduino integration potential.
* [CAN-RE-Tool](https://github.com/openvehicles/CAN-RE-Tool) - Reverse engineering tool for CAN bus systems, compatible with Arduino.

## Test Equipment and Simulators

* [ECU-simulator](https://github.com/lbenthins/ecu-simulator) - Simulates vehicle diagnostic services, testable with Arduino OBD-II setups.
* [ELM327-emulator](https://github.com/Ircama/ELM327-emulator) - Emulator for testing OBD-II dongles, usable with Arduino interfaces.

## Protocols

### OBD-II Tools

* [Arduino-OBD2-Async](https://github.com/v-ivanyshyn/Arduino-OBD2-Async) - Arduino library for asynchronous OBD-II data reading over CAN bus.
* [CAN-Shark](https://github.com/quantyle/CAN-Shark) - Works with OBD PIDs from Arduino + MCP2515 shield.
* [arduino-OBD2](https://github.com/sandeepmistry/arduino-OBD2) - Arduino library for reading OBD-II data from cars over CAN bus.
* [arduino-ecu-logger](https://github.com/ihaque/arduino-ecu-logger) - Arduino-based OBD2 engine monitor and data logger.

### J1939 Tools

* [J1939-CANBUS](https://github.com/taha842/J1939-CANBUS) - Supports engines like CAT, Perkins, etc., adaptable for Arduino with CAN shields.
* [python-j1939](https://github.com/milhead2/python-j1939) - J1939 support with python-can, can be interfaced with Arduino data.
* [Open-SAE-J1939](https://github.com/DanielMartensson/Open-SAE-J1939) - Free J1939 protocol for embedded systems, including Arduino.

## Utils

### Common

* 🔝[cantools](https://github.com/mwkpe/cantools) - CLI tools for CAN bus, useful for Arduino project analysis.
* [BUSMASTER](https://github.com/rbei-etas/busmaster) - Open-source tool to simulate and analyze CAN bus, compatible with Arduino data.

### Arduino-Specific

* [Arduino-canbus-monitor](https://github.com/latonita/arduino-canbus-monitor) - CAN bus monitoring tool based on Arduino and CAN bus shield.
* [slcanuino](https://github.com/kahiroka/slcanuino) - USB-CAN (SocketCAN) sketch for Arduino CAN-BUS shield.

### Libraries

* 🔝[arduino-mcp2515](https://github.com/autowp/arduino-mcp2515) - Arduino MCP2515 CAN interface library.
* [Arduino-STM32-CAN](https://github.com/nopnop2002/Arduino-STM32-CAN) - CAN communication example for Arduino Core STM32.
* [eXoCAN](https://github.com/exothink/eXoCAN) - CAN library for the STM32F103 (Blue Pill) with Arduino support.
* [FlexCAN](https://github.com/collin80/FlexCAN_Library) - Arduino library for CAN on Teensy, adaptable for other boards.

### Examples

* [CAN-Examples](https://github.com/craigpeacock/CAN-Examples) - Example C code for CAN sockets, adaptable for Arduino.
* [Arduino-CAN-bus-SD-logger](https://github.com/DieselDuz42/Arduino-CAN-bus-SD-logger) - Arduino script to log CAN bus data to SD card.

## CAN Database

### Formats (DBC, KCD)

#### DBC

* [DBC Format Specification v1.0](http://read.pudn.com/downloads766/ebook/3041455/DBC_File_Format_Documentation.pdf) - Leaked DBC file format spec.
* [cabana](https://github.com/commaai/cabana) - CAN visualizer and DBC maker, usable with Arduino data.

#### KCD

* [KCD](https://github.com/julietkilo/kcd) - Open XML-based CAN description format, similar to DBC.

### Converters and Parsers

* 🔝[cantools by Erik Moqvist](https://github.com/eerimoq/cantools) - Python tools for DBC, KCD parsing, useful with Arduino projects.
* [canmatrix](https://github.com/ebroecker/canmatrix) - Converts CAN database formats, integrable with Arduino workflows.

### DBC Only

* [dbc_reader](https://github.com/autti/dbc_reader) - Virtual CAN bus reader from DBC files, compatible with Arduino data.

## Hardware

### Arduino

* 🔝[arduino-canhacker](https://github.com/autowp/arduino-canhacker) - CanHacker CAN adapter on Arduino + MCP2515.
* [open-usb-can from Fabio Baltieri](https://github.com/fabiobaltieri/open-usb-can) - CAN-to-USB dongle based on ATMega32U and MCP2515.
* [CANBus-Triple](https://github.com/CANBus-Triple/CANBus-Triple-Hardware) - Car hacking platform based on AVR and MCP2515, with firmware support.
* [GVRET](https://github.com/collin80/GVRET) - Generalized Electric Vehicle Reverse Engineering Tool (Arduino FW).
* [CITM02](https://github.com/BXProject/CITM02) - Dual channel CANBUS adapter built around Arduino.
* [Arduino-psa-comfort-can-adapter](https://github.com/ludwig-v/arduino-psa-comfort-can-adapter) - Arduino sketch for PSA comfort devices on CAN-BUS.
* [epasuino](https://github.com/srenner/epasuino) - Arduino-based speed-sensitive electric power steering.
* [carfuino](https://github.com/srenner/carfuino) - Arduino-based automotive performance computer.
* [W203-canbus](https://github.com/rnd-ash/W203-canbus) - Arduino project for Mercedes W203/W211 bluetooth control.

### Hardware-Related Tools

* [CAN Bus Bit Timing Calculator](https://www.kvaser.com/support/calculators/bit-timing-calculator/) - Online tool for MCP2515 timing settings.

---

## Contributing

* Your contributions are always welcome! Please read the [contribution guidelines](contributing.md) first.

## Footnotes

1. Please follow [this](https://github.com/iDoka/awesome-canbus) root-repo for latest updates.
2. The another awesome list :arrow_forward: [CAN ID collections](https://github.com/iDoka/awesome-automotive-can-id) :arrow_backward: also might be useful.
3. Also might be useful [this curated list](https://github.com/iDoka/awesome-linbus) of awesome tools and resources for LIN bus.
