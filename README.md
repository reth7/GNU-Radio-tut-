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
ifconfig (interface configuration) command is used to configure the kernel-resident network interfaces
```bash
ifconfig
```
To find the available connected USRP devices:  
```bash
uhd_usrp_probe
```
To list all the available wireless networks
To list all the available wireless networks using a custom device(USRP) using a USRP device ID (enp03 in this case)
```bash
iwlist
```
In my system, running above command shows `enp0s3` device

```bash
iwlist enp0s3 scan
```


## Ethtool
The ethtool is a command-line tool in Linux for managing network interface devices. It allows us to modify the parameters of the devices and query the information of those devices.

```bash
sudo apt-get install -y ethtool
```
To get the general properties of a network interface device, we simply run ethtool followed by its name:


```
sudo ethtool enp0s3
```

```
Settings for enp0s3:
	Supported ports: [ TP ]
	Supported link modes:   10baseT/Half 10baseT/Full 
	                        100baseT/Half 100baseT/Full 
	                        1000baseT/Full 
	Supported pause frame use: No
	...
```
