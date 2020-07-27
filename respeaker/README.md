## ReSpeaker Based Activities

## Hardware

|Device|Cost|
|--|--|
|[Raspberry Pi Zero WH](https://www.adafruit.com/product/3708)|$14.00|
|[Micro SD Card 8GB](https://www.newegg.com/sandisk-8gb-microsdhc/p/0DF-0005-00190)|$6.00
|[ReSpeaker 2-Mic Pi HAT](https://www.digikey.com/product-detail/en/seeed-technology-co.,-ltd/107100001/1597-1513-ND/7325257)|$10.00|
|[Mini HDMI Adapter](https://www.adafruit.com/product/2819)|$3.00|
|[MicroB OTG male to USB-A male Adapter](https://www.adafruit.com/product/1099)|$2.50|
|[MicroB male to USB-A male Cable](https://www.adafruit.com/product/592)|$3.00|



## Software
- [Balena Etcher](https://www.balena.io/etcher/)
- [Rapsberry Pi OS Lite](https://www.raspberrypi.org/downloads/raspberry-pi-os/)

## Setup

1) Use [Balena Etcher](https://www.balena.io/etcher/) to flash Raspberry Pi OS image
2) Login to Raspberry Pi (user: pi, password: raspberry)
3) Run `sudo raspi-config`
    - Set networking settings
    - Change locale / keyboard settings
    - Enable SSH and SPI interfacing
    - Reboot and note IP address `<My-IP-Address>`
4) From computer on the same network ssh to Raspberry Pi
    - `ssh pi@<My-Ip-Address>`
5) Clone repo
    -  `sudo apt-get update && sudo apt-get install -y git python3-pip`
    - `git clone https://github.com/rpy-learn`
    - `cd rpy-learn/respeaker`
6) Run installation script (this takes a while)
    - `sudo install.sh`
7) Install python requirements (this takes a while)
    - pip3 install -r requirements.txt
8) Start the jupyter server
    - `jupyter notebook`
    - click on the link provided to open