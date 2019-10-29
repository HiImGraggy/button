## Preparing

  * Update APT caches and install common tools and libraries
```bash
sudo apt update
sudo apt install -y git vim arm-none-eabi-gcc libnewlib-arm-none-eabi minicom build-essential cmake libusb-1.0-0-dev
```

  * Install Linux [stlink tools](https://github.com/texane/stlink) using [this manual](https://github.com/texane/stlink/blob/master/doc/compiling.md)

  * Create work directory and add it to bash environment as a variable for fast access
```bash
mkdir ~/development
echo "export WORKDIR=~/development" >> ~/.bashrc
source ~/.bashrc
```

## Download example project

  * Clone project
```bash
cd $WORKDIR
git clone https://github.com/HiImGraggy/button
```

## Building and flashing firmware

  * Go to "button" sample folder
```bash
cd $WORKDIR/button/
```

  * Build firmware
```bash
make
```

  * Flash firmware to device. NOTE: starter kit should be powered and CN1 connected to PC
```bash
make flash
```
