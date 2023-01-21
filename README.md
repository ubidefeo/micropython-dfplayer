Introduction
============

Fork of https://github.com/bablokb/circuitpython-dfplayer

This is a library for the mini-dfplayer, a minimalistic MP3-player
available for a few bucks from Ebay, Amazon and other distributors.

![](assets/dfplayer.png)

The chip has a number of pins for direct control, but also an
UART-interface and this library controls the chip using the documented
commands.

The core of the code is from a micropython implementation of the interface
[https://github.com/jczic/KT403A-MP3](https://github.com/jczic/KT403A-MP3).

### IMPORTANT
There exist several versions of this SD Card mp3 player, and as many chips which are not compatible with each other.
This library works with YX5200.
If you want a reference to implement other chips, take a look at https://github.com/enjoyneering/DFPlayer/blob/main/src/DFPlayer.h


Installation
------------

Just copy the file `lib/DFPlayer.py` to your MicroPython board's root or inside its `lib` directory if Block Device is supported


Usage
-----

Import the library and create a `DFPlayer`-object. If you don't pass an
uart, the constructor defaults to UART 0.
Use the created object to control the player. For the API just have a
look at the source-code.

A real-world example can be found in the project:
[https://github.com/bablokb/xmas-music-box](https://github.com/bablokb/xmas-music-box).