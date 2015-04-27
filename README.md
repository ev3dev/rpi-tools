Raspberry Pi Tools
==================

This is a fork the "official" Raspberry Pi tools (for building kernel images)
from the Raspberry Pi foundation. This fork adds Debian packaging to make it
easier to install.

You can get the packages by adding one of the following to your
`/etc/apt/sources.list` file...

    # For i386 and amd64
    deb http://ev3dev.org/debian trusty main
    # For armel and armhf
    deb http://ev3dev.org/debian jessie main
    # For raspbian amrhf
    deb http://ev3dev.org/raspbian jessie main

You also need to install the public key with...

    sudo apt-key adv --keyserver pgp.mit.edu --recv-keys 2B210565

And don't for get to update...

    sudo apt-get update

Install the Raspbian (armv6) cross-build toolchain (i386 and amd64 only) with...

    sudo apt-get install gcc-linaro-arm-linux-gnueabihf-raspbian

The toolchain installs to `/usr/lib/gcc-linaro-arm-linux-gnueabihf-raspbian`.
It is not included in your `PATH` by default since it conflicts with Debian/Ubuntu
armhf (armv7) toolchains.

Install the `mkknlimg` and `knlinfo` tools with...

    sudo apt-get install rpi-mkimage
