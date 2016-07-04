# ESP8266 setup: sdk + toolchain

I hate the modular project structure used by Espressif for their SDK, so I made
one that looks more like a normal C project.

    project
        |- bin          # binaries (elf/archives/firmware)
        |- include      # C headers
        |- obj          # compiled objects
        |   \- drivers  # compiled objects for uart/i2c/... code from Espressif
        \- src          # source code
        
