# Pirate Radio Setup Instructions

Setup Instructions for the [Pirate Radio - Pi Zero WH Project Kit](https://shop.pimoroni.com/products/pirate-radio-pi-zero-w-project-kit?variant=38476372426) (as of 2026).

## Items to Prepare in Advance

The OS compatible with pHAT BEAT, which comes with Pirate Radio, is Bullseye (versions Bookworm and later are likely not compatible).

 - [2023-05-03-raspios-bullseye-armhf.img.xz](https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2023-05-03/)

Since wiringpi has become open-source on GitHub, download it in advance.

 - [wiringpi_3.14_bullseye_armhf.deb](https://github.com/WiringPi/WiringPi/releases/tag/3.14)

## OS Setup

Use the [Raspberry Pi Imager](https://www.raspberrypi.com/software/) to write the OS image to an SD card, then set up the OS and update the software.

\* Be sure to set the username to `pi`.

## pHAT BEAT Setup

Place the `phatbeat` and `wiringpi_3.14_bullseye_armhf.deb` files from this repository in the same folder.

Set the OS_NAME environment variable.

```sh
export OS_NAME=Raspbian

echo $OS_NAME
```

Next, run `phatbeat`.

```sh
chmod a+rx phatbeat

bash phatbeat
```

If a prompts you to restart, restart the system.

## VLC Setup

Merge the contents of the `Pimoroni` folder in this repository into `/home/pi/Pimoroni`.

Next, run `setup.sh`

```sh
cd Pimoroni/phatbeat/projects/vlc-radio/

./setup.sh
```
