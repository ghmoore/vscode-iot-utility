# IoT Utility

[![Join the chat at https://gitter.im/formulahendry/vscode-platformio](https://badges.gitter.im/formulahendry/vscode-platformio.svg)](https://gitter.im/formulahendry/vscode-platformio?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Marketplace Version](https://vsmarketplacebadge.apphb.com/version-short/formulahendry.platformio.svg)](https://marketplace.visualstudio.com/items?itemName=formulahendry.platformio) [![Installs](https://vsmarketplacebadge.apphb.com/installs-short/formulahendry.platformio.svg)](https://marketplace.visualstudio.com/items?itemName=formulahendry.platformio) [![Rating](https://vsmarketplacebadge.apphb.com/rating-short/formulahendry.platformio.svg)](https://marketplace.visualstudio.com/items?itemName=formulahendry.platformio) [![Build Status](https://travis-ci.org/formulahendry/vscode-platformio.svg?branch=master)](https://travis-ci.org/formulahendry/vscode-platformio)

Integrate [PlatformIO](http://platformio.org/) into Visual Studio Code on top of [PlatformIO Core](http://docs.platformio.org/en/stable/core.html). Cross-platform Build System without external dependencies to the OS software: 550+ embedded boards, 25+ development platforms, 15+ frameworks. Arduino and ARM mbed compatible.

*Atmel AVR & SAM, Espressif 8266 & 32, Freescale Kinetis, Intel ARC32, Lattice iCE40, Microchip PIC32, Nordic nRF51, NXP LPC, Silicon Labs EFM32, ST STM32, TI MSP430 & Tiva, Teensy, Arduino, ARM mbed, libOpenCM3, ESP8266, etc.*

## What's New in v0.3.0

**Discover devices connected via Ethernet, Wi-Fi and USB**: Press `F1` and then select/type `IoT Utility: Discover Device`. (Make sure you have installed [device-discovery-cli](https://github.com/Azure/device-discovery-cli))

```
	IP Address    MAC Address       Type                                    Host Name

	10.172.14.69  08:00:27:d7:27:ef raspberrypi (Raspberry Pi)              raspberrypi
	10.172.15.84  00:15:5d:0f:9d:01 tessel (Tessel 2)                       tessel2
	10.172.14.219 00:0c:29:35:fa:9f huzzah (Adafruit HUZZAH ESP8266)
	10.172.15.98  78:2b:cb:b5:1c:9c ?
```

## Note

If you want to build IoT projects connected to an IoT cloud service. You could take a look at [aka.ms/azure.iot](https://aka.ms/azure.iot) for Microsoft Azure IoT projects and resources.

If you are already using Azure IoT services, you could use [Azure IoT Toolkit](https://marketplace.visualstudio.com/items?itemName=vsciot-vscode.azure-iot-toolkit) extension for better development experience.

## Features

* Build PlatformIO project specified in [Project Configuration File platformio.ini](http://docs.platformio.org/en/stable/projectconf.html#projectconf)
* Upload firmware to devices specified in [Project Configuration File platformio.ini](http://docs.platformio.org/en/stable/projectconf.html#projectconf)
* Open Serial Monitor
* Set baud rate for Serial Monitor
* Search for library in [PlatformIO Library Registry](http://platformio.org/lib)
* Install library from [PlatformIO Library Registry](http://platformio.org/lib)
* Quick way to open PlatformIO Terminal
* Automatically or manually add Include Path to `c_cpp_properties.json` for [C/C++ extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
* Combined `Build`, `Upload` and `Open Serial Monitor` with one command
* Discover devices connected via Ethernet, Wi-Fi and USB

## Prerequisites

* Install [PlatformIO Core](http://docs.platformio.org/en/stable/installation.html)

## Setup

* Use existing project

  If you have an existing PlatformIO project, open the project folder directly in VS Code

* Create new project

  In terminal, run `platformio init --board <your_board_identifier>` to initialize a new PlatformIO project, then open the project folder in VS Code. Refer to [User Guide](http://docs.platformio.org/en/stable/userguide/cmd_init.html) for `platformio init` command. For how to find Board Identifier, you could refer to [this](http://docs.platformio.org/en/stable/quickstart.html#board-identifier).

## Usage

* **Build PlatformIO project**: Use shortcut `Ctrl+Alt+B`, or press `F1` and then select/type `PlatformIO: Build`, or right click the Text Editor and then click `PlatformIO: Build` in context menu

![build](images/build.gif)

* **Upload firmware to devices**: Use shortcut `Ctrl+Alt+U`, or press `F1` and then select/type `PlatformIO: Upload`, or right click the Text Editor and then click `PlatformIO: Upload` in context menu

![upload](images/upload.gif)

* **Open Serial Monitor**: Use shortcut `Ctrl+Alt+S`, or press `F1` and then select/type `PlatformIO: Open Serial Monitor`, or right click the Text Editor and then click `PlatformIO: Open Serial Monitor` in context menu

![openSerialMonitor](images/openSerialMonitor.gif)

* **Search for library**: Click the `Library` item in the Status Bar at the bottom, or press `F1` and then select/type `PlatformIO: Search Library`, then type the query to search for library. Refer to the [User Guide](http://docs.platformio.org/en/latest/userguide/lib/cmd_search.html#description) for the query syntax.

![searchLibrary](images/searchLibrary.gif)

* **Install library**: Click the `Download` icon in the Status Bar at the bottom, or press `F1` and then select/type `PlatformIO: Install Library`, then type library id or name to install. Refer to the [User Guide](http://docs.platformio.org/en/latest/userguide/lib/cmd_install.html#usage) for the detailed usage.

![installLibrary](images/installLibrary.gif)

* **Quick way to open PlatformIO Terminal**: Click the `Terminal` icon in the Status Bar at the bottom, or press `F1` and then select/type `PlatformIO: Open Terminal`

![openTerminal](images/openTerminal.png)

* **Add Include Path to `c_cpp_properties.json` for C/C++ extension**: Press `F1` and then select/type `PlatformIO: Add Include Path to Settings`. Wait for some seconds, then the PlatformIO libraries will be automatically added into Include Path of `c_cpp_properties.json`. (**Note**: Do not modify `c_cpp_properties.json` manually since the `c_cpp_properties.json` will be fully regenerated and your manual changes will be lost.)

* **Combined `Build`, `Upload` and `Open Serial Monitor` with one command**: Click the `Right Arrow` icon in the Status Bar at the bottom, or use shortcut `Ctrl+Alt+A`, or press `F1` and then select/type `PlatformIO: Build, Upload and Open Serial Monitor`. `Build`, `Upload` and `Open Serial Monitor` will be run one by one.

![buildUploadAndOpenSerialMonitor](images/buildUploadAndOpenSerialMonitor.png)

* **Discover devices connected via Ethernet, Wi-Fi and USB**: Press `F1` and then select/type `IoT Utility: Discover Device`. (Make sure you have installed [device-discovery-cli](https://github.com/Azure/device-discovery-cli))

```
	IP Address    MAC Address       Type                                    Host Name

	10.172.14.69  08:00:27:d7:27:ef raspberrypi (Raspberry Pi)              raspberrypi
	10.172.15.84  00:15:5d:0f:9d:01 tessel (Tessel 2)                       tessel2
	10.172.14.219 00:0c:29:35:fa:9f huzzah (Adafruit HUZZAH ESP8266)
	10.172.15.98  78:2b:cb:b5:1c:9c ?
```

## Settings

* `platformio.baudRate`: Set baud rate for Serial Monitor. (Default is **9600**)
* `platformio.showHelpInfo`: Whether to show help info when opening PlatformIO Terminal. (Default is **true**)
* `platformio.autoUpdateIncludes`: Whether to add Include Path to `c_cpp_properties.json` automatically. (Default is **true**)

## Telemetry data

By default, anonymous telemetry data collection is turned on to understand user behavior to improve this extension. To disable it, update the settings.json as below:
```json
{
    "platformio.enableTelemetry": false
}
```

## Change Log

See Change Log [here](CHANGELOG.md)

## Issues

Currently, the extension is in the very initial phase. If you find any bug or have any suggestion/feature request, please join the chat on [Gitter](https://gitter.im/formulahendry/vscode-platformio) or submit the [issues](https://github.com/formulahendry/vscode-platformio/issues) to the GitHub Repo.

## Contributions

Contributions are warmly welcome! Please follow the [Contribution Guide](CONTRIBUTING.md) to setup development environment. 
