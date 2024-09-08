# atommc3

An experimental raspberry pi pico SD card interface for the Acorn Atom.

[Licensed under CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/)

Note: Installing and using the vscode-pico extension seems to really mess up the build - to the extent that . But it does build using the Manual toolchain setup in: https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf

~~~bash
cd build
cmake -DPICO_BOARD=pico ..
make
~~~
