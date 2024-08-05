## REQUIREMENTS
- preinstalled and setup of openocd
# if openocd not present in linux then follow below procedure to install and setup of openocd:
- `sudo apt-get install autoconf automake libtool`
- `git clone https://github.com/ntfreak/openocd.git`
- `cd openocd`
- `./bootstrap`
- `./configure --enable-maintainer-mode`
- `make`
- `sudo make install`

# how to write hex into pinaka from hex sem_hub.hex and sem_dc.hex using pinaka.cfg?:

- download files pinaka.cfg, sem_hub.hex, sem_dc.hex in one folder
- go to the same folder in terminal and write below command
- for sem hub `openocd -f pinaka.cfg -c "reset init" -c "load_image sem_hub.hex;resume 0x80000000; shutdown"`
- for sem dc `openocd -f pinaka.cfg -c "reset init" -c "load_image sem_dc.hex;resume 0x80000000; shutdown"`
