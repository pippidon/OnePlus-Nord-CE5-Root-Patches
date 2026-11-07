# For APatch

## Info

If you're using APatch, you need to patch your own image due to it requiring a SuperKey.

## Guide

1. Go to the stock images folder and grab the *boot.img* file
2. Install *APatch* (if you haven't already) and patch the *boot.img*
3. If you have already unlocked the bootloader (as described in the main tutorial), you need to reboot into fastboot
  ```bash
  adb reboot bootloader
  ```
or
  ```bash
  adb reboot fastboot
  ```
4. After booting into fastboot, you need to run this command
  ```bash
  fastboot flash boot <path/to/file.img>
  ```
