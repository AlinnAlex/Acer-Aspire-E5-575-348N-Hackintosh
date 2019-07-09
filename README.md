[![Screenshot-2019-07-09-at-11-17-46.png](https://i.postimg.cc/C5MTdVDm/Screenshot-2019-07-09-at-11-17-46.png)](https://postimg.cc/CB266Xcq)
# Acer-Aspire-E5-575-348N-Hackintosh

## Please note that you will need a compatible Broadcom wifi card or an usb adapter, otherwise wifi wouldn't work. I use TPLINK TL-WN725N.

## Installation

- The config.plist is configured for Intel HD 520 and Realtek ALC255 for audio. If you have another integrated GPU please choose a proper config.plist from [here!](https://github.com/RehabMan/OS-X-Clover-Laptop-Config)
- To create a bootable usb you will need a real Mac to download the full installer. If you don't have access to real Mac you can use a Mac VM in VirtualBox. You can follow [this](https://www.saintlad.com/install-macos-sierra-in-virtualbox-on-windows-10/). 
- Create an installation media using this [guide!](https://www.tonymacx86.com/threads/guide-booting-the-os-x-installer-on-laptops-with-clover.148093/).
- Download or clone and move contents to CLOVER EFI.
- Install.

## Post-install
- Install kexts from kexts/other to /Library/Extensions/ using kextbeast.
- move contents from the bootable usb CLOVER EFI partition to local EFI partition 
    1. `sudo mkdir /Volumes/EFI && sudo mount -t msdos /dev/disk0s1 /Volumes/EFI`
    2. `cp -R "/Volumes/CLOVER EFI" /Volumes/EFI`
- run `sudo trimforce enable` if you have a SSD;
- disable auto updates

## Credits 

[Rehabman!](https://github.com/RehabMan)
[Acidanthera!](https://github.com/acidanthera)
[Clover Bootloader!](https://sourceforge.net/projects/cloverefiboot/)
