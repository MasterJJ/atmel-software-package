trouble shooting
-----------------


build  example getstarted  
make TARGET=sama5d2-xplained

## error 1

/usr/lib/gcc/arm-none-eabi/6.3.1/../../../arm-none-eabi/bin/ld: error: build/sama5d2-xplained/sram/getting-started.elf uses VFP register arguments, /usr/lib/gcc/arm-none-eabi/6.3.1/../../../arm-none-eabi/lib/libc_nano.a(lib_a-atexit.o) does not

## soultion -1

sudo apt-get remove gcc-arm-none-eabi binutils

#### ubuntu > 16.04

sudo add-apt-repository ppa:team-gcc-arm-embedded/ppa
sudo apt-get update
sudo apt-get install gcc-arm-embedded


#### ubuntu < 16.04

sudo add-apt-repository ppa:terry.guo/gcc-arm-embedded
sudo apt-get update
sudo apt-get install arm-gcc-none-eabi


#### tip -1

package install error return code 1

dpkg install error return code 1

sudo dpkg --force-all -i /var/cache/apt/archives/gcc-arm-embedded_7-2018q2-1~bionic1_amd64.deb

