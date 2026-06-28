# ESP32-S3 Testboard

## Overview

This project is a custom ESP32-S3 testboard designed in KiCad. The board was created as a compact development and testing platform for the ESP32-S3-WROOM module.

The board includes USB-C power and data connection, 3.3 V voltage regulation, boot and reset buttons, a user button, RGB LED, Qwiic I2C connector, GPIO headers, and an onboard Si7021-A20 temperature and humidity sensor.

The purpose of this project is to practice PCB design, ESP32-S3 hardware design, sensor integration, and GitHub-based engineering documentation.

## Main Features

* ESP32-S3-WROOM module
* USB-C connector for power and USB communication
* 5 V input from USB-C
* 3.3 V regulated power supply
* Boot and reset buttons
* User button
* RGB LED
* Si7021-A20 temperature and humidity sensor
* Qwiic I2C connector
* GPIO/SPI breakout headers
* ESD protection components
* Mounting holes
* ESP32-S3 antenna keepout area

## Hardware Description

### ESP32-S3 Module

The main microcontroller of the board is the ESP32-S3-WROOM module. It provides Wi-Fi, Bluetooth Low Energy, GPIO, USB, I2C, SPI, UART, PWM, ADC, and other peripheral interfaces.

The board exposes several ESP32-S3 pins through headers so the module can be used for testing and prototyping.

### Power Supply

The board is powered through the USB-C connector. The USB 5 V input is protected using a polyfuse and then regulated to 3.3 V using an LDO regulator.

The 3.3 V rail powers the ESP32-S3 module, Si7021 sensor, RGB LED, Qwiic connector, and supporting circuits.

### USB-C Interface

The USB-C connector provides power and USB data communication. The USB D+ and D− lines are connected to the ESP32-S3 USB pins for programming and serial communication.

### Boot and Reset Circuit

The board includes dedicated boot and reset buttons. The boot button is connected to GPIO0, and the reset button is connected to the ESP32-S3 enable/reset line.

These buttons allow the ESP32-S3 to be reset and placed into programming mode during firmware upload.

### Si7021 Temperature and Humidity Sensor

The board includes the Si7021-A20 digital temperature and humidity sensor. It communicates with the ESP32-S3 using the I2C bus.

This sensor can be used for:

* Temperature measurement
* Humidity measurement
* Environmental monitoring
* I2C communication testing

### Qwiic I2C Connector

A Qwiic connector is included for connecting external I2C modules. The connector provides:

* GND
* 3.3 V
* SDA
* SCL

Pull-up resistors are included on the I2C lines.

### RGB LED

The RGB LED is connected to ESP32-S3 GPIO pins through current-limiting resistors. It can be used for status indication, firmware testing, and GPIO output testing.

## Repository Structure

```text
ESP32-S3-Testboard/
│
├── README.md
├── .gitignore
│
├── kicad/
│   ├── ESP32-S3.kicad_pro
│   ├── ESP32-S3.kicad_sch
│   └── ESP32-S3.kicad_pcb
│
├── Images/
│   ├── schematic.png
│   ├── pcb_layout.png
│   └── pcb_3d_view.png
│
├── Documentation/
│   └── Datasheets/
│       ├── esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf
│       └── Si7021-A20_datasheet.pdf
│
└── Manufacturing/
    ├── Gerbers/
    └── Drill/
```

## KiCad Project

The KiCad design files are located in the `kicad/` folder.

To open the project:

1. Install KiCad.
2. Open the `.kicad_pro` file.
3. Review the schematic and PCB layout.
4. Run ERC and DRC before modifying or manufacturing the board.

## Images

Project images are located in the `Images/` folder.

Included images:

* Schematic screenshot
* PCB layout screenshot
* 3D PCB render

## Manufacturing

Manufacturing files will be placed in the `Manufacturing/` folder.

Before ordering the PCB, the following checks should be completed:

* Electrical Rules Check
* Design Rules Check
* Gerber preview inspection
* Drill file verification
* USB-C footprint check
* ESP32-S3 footprint orientation check
* ESP32-S3 antenna keepout check
* Power trace width check
* I2C pull-up resistor verification

## Project Status

* [x] Schematic completed
* [x] PCB layout completed
* [x] ESP32-S3 module added
* [x] USB-C interface added
* [x] 3.3 V regulator added
* [x] Si7021 sensor added
* [x] Qwiic connector added
* [x] RGB LED added
* [ ] PCB manufactured
* [ ] Board assembled
* [ ] Power supply tested
* [ ] USB programming tested
* [ ] Si7021 sensor tested
* [ ] Example firmware added

## Author

Ali Sarp Aksoy
Mechatronics Engineering Student
Kraków, Poland
