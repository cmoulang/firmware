# firmware for atom-pico-SDcard interface

An _experimental_ raspberry pi pico SD card interface for the Acorn Atom.

 This is a modified version of the micro controller firmware at: https://github.com/hoglet67/AtoMMC2Firmware 

[Licensed under CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/)

Note: Installing and using the otherwise brilliant vscode-pico extension seems to do weird stuff and really messes up the build (probably something I've done). But the project does build using the Manual toolchain setup in: https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf

~~~bash
# Building and testing commands

# Build for pico 2
cd build2
cmake -DPICO_BOARD=pico2 ..
make

# Build for original pico
cd build
cmake -DPICO_BOARD=pico ..
make

# debugprobe - use rp2040 for original pico
sudo openocd -f interface/cmsis-dap.cfg -f target/rp2350.cfg -c "adapter speed 5000"

gdb-multiarch -ex "target extended-remote localhost:3333" rpipFirmware3.elf

minicom -b 115200 -o -D /dev/ttyACM0

~~~
