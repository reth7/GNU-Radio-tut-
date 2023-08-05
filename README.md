# GNU Radio Application

This repo explains the installation of GNU radio along with some basic applications which can be executed on a USRP device [Universal Software Radio Peripheral (USRP) devices are software defined radios (SDR) used for RF applications].

## Installation of GNU Radio

 - I am using Ubuntu 21.10 
First we are going to install UHD library

[USRPs are transceivers, meaning that they can both transmit and receive RF signals. UHD provides the necessary control used to transport user waveform samples to and from USRP hardware as well as control various parameters (e.g. sampling rate, center frequency, gains, etc) of the radio.]


```bash
sudo apt update
sudo apt -y install uhd-host
```
Now we add GNU repository 

```bash
sudo add-apt-repository ppa:gnuradio/gnuradio-releases-3.9
```
Make sure you have python-3 packaging installed
I didn't have python3 so I installed it with GNU Radio
```bash
sudo apt-get update
sudo apt-get install gnuradio python3-packaging
```
Installing GNU Radio
```bash
sudo apt update
sudo apt upgrade
sudo apt install gnuradio
```
To see the available UHD devices: 
```bash 
uhd_find_devices
```
To see the available connections 
```bash
ifconfig
```
