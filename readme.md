# ESP8266 sdk + toolchain: my setup

I hate the modular projects structure used by Espressif for their SDK, 
so I made a makefile to use a more standard C project.

    - project
        |- bin          # binaries (elf/firmware)
        |- include      # C headers
        |- lib          # C libraries
        |- obj          # compiled objects
        |   \- drivers  # compiled objects for uart/i2c/... code from Espressif
        \- src          # source code

## Setup

Download this repo recursively and build every submodule

    $ git clone --recursive https://github.com/NaoPross/esp8266-setup
     
    $ cd esp-open-sdk
    $ make

    $ cd ../esptool-ck
    $ make

To test if everything works try to build the template project

    $ cd projects/template
    $ make
