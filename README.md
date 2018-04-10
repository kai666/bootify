# bootify

bootify is a Bash script to make bootable USB drives with Windows 7/8/10 
installation files. It can be used for Boot or UEFI systems.

## Dependencies

Make sure the following tools exist on your system:

* `stat`
* `file`
* `lsblk`
* `dd`
* `mkfs.ntfs`
* `mkfs.vfat`
* `parted`
* `7z`
* `rsync`

## Usage

Make sure `bootify.sh` is executable: `chmod +x bootify.sh`

`sudo ./bootify.sh -d [DEVICE] -s [boot|uefi] -i [ISO]`

## Todo

* Provide a nice progress indicator
* Handle interruption events

## Bugs

* Old `lsblk` versions have less available columns to report device data. The script will crash if your system uses them.
* You can't use Windows 7 32bits in UEFI mode. UEFI is supported from Windows 7 64bits onwards. If you try to make a USB bootable using Windows 7 32bits it will never work.
