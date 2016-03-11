Raspberry Pi Tools
==================

This is a fork the "official" Raspberry Pi tools (for building kernel images)
from the Raspberry Pi foundation. This fork adds Debian packaging to make it
easier to install.

You can get the packages by adding the ev3dev.org Ubuntu package repository to
your `/etc/apt/sources.list` file...

    sudo apt-add-repository "deb http://ev3dev.org/ubuntu trusty main

You also need to install the public key with...

    sudo apt-key adv --keyserver pgp.mit.edu --recv-keys 2B210565

And don't for get to update...

    sudo apt-get update

Install the Raspbian (armv6) cross-build toolchain (amd64 only) with...

    sudo apt-get install gcc-arm-rpi-4.9.3-linux-gnueabihf

The toolchain installs to `/usr/lib/x86_64-linux-gnu/gcc-arm-rpi-4.9.3-linux-gnueabihf`.
It is not included in your `PATH` by default since it conflicts with Debian/Ubuntu
armhf (armv7) toolchains.
