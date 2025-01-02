# Atmel AVR: development platform for [PlatformIO](https://platformio.org)

<!--[![Build Status](https://github.com/modern-avr/platform/workflows/Examples/badge.svg)](https://github.com/modern-avr/platform/actions)-->

This is a fork that adds support for modern C++ versions and the C++ standard library (freestanding implementation). This makes it possible to use C++26 on AVR.

## What Does It Change?

Aside from providing a newer compiler, it makes a few changes to the build flags:

### For C++:
- Replaces `-std=gnu++11` with `-std=gnu++26`.
- Removes `-fpermissible` to encourage better coding practices.
- Adds `-Wno-volatile` because Arduino framework uses `volatile` in a now deprecated way.

### For C:
- Replaces `-std=gnu11` with `-std=gnu23`.

You can re-enable or disable any flags using `build_flags` and `build_unflags`, as usual.

---

Atmel AVR 8- and 32-bit MCUs deliver a unique combination of performance, power efficiency and design flexibility. Optimized to speed time to market-and easily adapt to new ones-they are based on the industrys most code-efficient architecture for C and assembly programming.

Documentation related to the **upstream platform** (`platform-atmelavr`):

* [Home](https://registry.platformio.org/platforms/platformio/atmelavr) (home page in the PlatformIO Registry)
* [Documentation](https://docs.platformio.org/page/platforms/atmelavr.html) (advanced usage, packages, boards, frameworks, etc.)

# Usage

1. [Install PlatformIO](https://platformio.org)
2. Create PlatformIO project and configure a platform option in [platformio.ini](https://docs.platformio.org/page/projectconf.html) file:

## Stable version

```ini
[env:stable]
platform = https://github.com/modern-avr/platform.git
board = ...
...
```

## Specific version

```ini
[env:v14.2.0]
platform = https://github.com/modern-avr/platform.git#v14.2.0
board = ...
...
```

## Development version

```ini
[env:development]
platform = https://github.com/modern-avr/platform.git#develop
board = ...
...
```

# Configuration

Please navigate to [documentation of the upstream platform](https://docs.platformio.org/page/platforms/atmelavr.html).
