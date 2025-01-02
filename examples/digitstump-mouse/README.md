How to build PlatformIO based project
=====================================

1. [Install PlatformIO Core](https://docs.platformio.org/page/core.html)
2. Download [development platform with examples](https://github.com/modern-avr/platform/archive/develop.zip)
3. Extract ZIP archive
4. Run these commands:

```shell
# Change directory to example
$ cd platform/examples/digitstump-mouse

# Build project
$ pio run

# Upload firmware
$ pio run --target upload

# Build specific environment
$ pio run -e digispark-tiny

# Upload firmware for the specific environment
$ pio run -e digispark-tiny --target upload

# Clean build files
$ pio run --target clean
```
