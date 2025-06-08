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
