
# timelapse1090

- timelapse web interface for dump1090-fa
- does not interfere with the existing dump1090-fa installation
- check out which plane flew by an hour or even 8 hours ago


![Screenshot](https://raw.githubusercontent.com/adsbfi/timelapse1090/screenshots/interface.png)

## Installation

```
sudo bash -c "$(wget -q -O - https://raw.githubusercontent.com/adsbfi/timelapse1090/master/install.sh)"
```

## View the added webinterface

Click the following URL and replace the IP address with address of your Raspberry Pi:

http://192.168.x.yy/timelapse

**Note: Website loading time can be up to a minute, if you want to reduce that you can reduce the duration saved or increase the interval of data points**

## Configuration (optional):

Edit the configuration file to change the interval and total duration of history saved:
```
sudo nano /etc/default/timelapse1090
```
Ctrl-x to exit, y (yes) and enter to save.

Apply the configuration:
```
sudo systemctl restart timelapse1090
```

## Deactivate / uninstall:

```
sudo systemctl disable --now timelapse1090
```
