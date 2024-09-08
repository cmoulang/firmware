# firmware for atom-pico-SDcard interface

An _experimental_ raspberry pi pico SD card interface for the Acorn Atom.

 This is a modified version of the micro controller firmware at: https://github.com/hoglet67/AtoMMC2Firmware 

[Licensed under CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/)

Note: Installing and using the otherwise brilliant vscode-pico extension seems to do weird stuff and really messes up the build. But it does build using the Manual toolchain setup in: https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf

~~~bash
cd build
cmake -DPICO_BOARD=pico ..
make
~~~
