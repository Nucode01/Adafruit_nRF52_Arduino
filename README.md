# Arduino Core for NUCODE nRF52 Boards

[![Build Status](https://github.com/adafruit/Adafruit_nRF52_Arduino/workflows/Build/badge.svg)](https://github.com/adafruit/Adafruit_nRF52_Arduino/actions)

This repository contains the Arduino BSP for NUCODE nRF52 series:

- [NU40DK nRF52840](https://nucode.gitbook.io/nuseries/ble-zigbee-thread-module-and-dk/nu40)

## BSP Installation

There are two methods that you can use to install this BSP. We highly recommend the first option unless you wish to participate in active development of this codebase via Github.

### Recommended: NUCODE nRF52 BSP via the Arduino Board Manager

 1. [Download and install the Arduino IDE](https://www.arduino.cc/en/Main/Software) (At least v1.6.12)
 2. Start the Arduino IDE
 3. Go into Preferences
 4. Add https://github.com/nucode01/Adafruit_nRF52_Arduino/blob/master/package_nuduino_index.json as an 'Additional Board Manager URL'
 5. Restart the Arduino IDE
 6. Open the Boards Manager from the Tools -> Board menu and install 'NUBoards nRF52 by NUCODE'

### Adafruit's nrfutil tools

[adafruit-nrfutil](https://github.com/adafruit/Adafruit_nRF52_nrfutil) (derived from Nordic [pc-nrfutil](https://github.com/NordicSemiconductor/pc-nrfutil)) is needed to upload sketch via serial port.

- For Windows and macOS, pre-built executable binaries are included in the BSP at `tools/adafruit-nrfutil/`. It should work out of the box.
- Linux user need to run follow command to install it from PyPi

```
$ pip3 install adafruit-nrfutil --user
```

### Burning new Bootloader

#### Updating

## Credits

This core is based on [Adafruit_nRF52_Arduino](https://github.com/adafruit/Adafruit_nRF52_Arduino) by Adafruit, which in turn is based on [Arduino-nRF5](https://github.com/sandeepmistry/arduino-nRF5) by Sandeep Mistry, which in turn is based on the [Arduino SAMD Core](https://github.com/arduino/ArduinoCore-samd).

The following libraries are used:

- [FreeRTOS](https://www.freertos.org/) as operating system
- [LittleFS](https://github.com/ARMmbed/littlefs) for internal file system
- [nrfx](https://github.com/NordicSemiconductor/nrfx) for peripherals driver
- [TinyUSB](https://github.com/hathach/tinyusb) as usb stack
