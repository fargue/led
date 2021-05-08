# README.md

## Links

[Tutorial](https://tutorials-raspberrypi.com/connect-control-raspberry-pi-ws2812-rgb-led-strips/)

```
sudo apt-get update
sudo apt-get install gcc make build-essential python-dev git scons swig
```

* disable audio
```
sudo nano /etc/modprobe.d/snd-blacklist.conf
```

add the following line:

`blacklist snd_bcm2835`

`sudo nano /boot/config.txt`

comment out this line:

#dtparam=audio=on

reboot

sudo reboot

clone the library:

git clone https://github.com/jgarff/rpi_ws281x
cd rpi_ws281x/
sudo scons

cd python

sudo python3 setup.py build 
sudo python3 setup.py install 
sudo pip3 install adafruit-circuitpython-neopixel

sudo nano examples/strandtest.py

sudo python3 examples/strandtest.py