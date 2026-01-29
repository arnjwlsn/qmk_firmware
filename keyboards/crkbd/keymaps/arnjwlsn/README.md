# arnjwlsn's Corne layout

## Compiling

```sh
./util/docker_build.sh clean
./util/docker_build.sh crkbd:arnjwlsn
```

## Flashing

```sh
./util/docker_build.sh crkbd:arnjwlsn:flash
```

### Enable Bootloader Mode
Boot loading mode must be enabled when flashing the keyboard. Press the button
next to the right screen to enable this. 

In the past, the computer was unable to recognize and communicate with the 
keyboard's bootloader. 

1. `sudo wget -O /etc/udev/rules.d/50-qmk.rules https://raw.githubusercontent.com/qmk/qmk_firmware/master/util/udev/50-qmk.rules`
2. `sudo udevadm control --reload-rules`
3. `sudo udevadm trigger`
