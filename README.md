# Info

Discord - valenvnovel 

Contains patched *init_boot* images for many root solutions

Also contains stock *init_boot.img* and *boot.img* for APatch users (see the [APatch guide](https://github.com/valenrina/OnePlus-Nord-CE5-Root-Patches/blob/main/Rooted%20images/For%20Apatch%20Users.md))

Currently only for **CPH2719_16.0.5.1002(EX01)** firmware version

## Root solutions

- Magisk
- KernelSU
- KernelSU-Next
- Wild KSU
- SukiSU Ultra
- ReSukiSu
- Kitsune Mask (Magisk Delta)
- Magisk Alpha

I also wanted to add APatch here, but it requires a **SuperKey**, so that's why there is a stock boot.img included in the *Stock images* folder

# Guide

WARNING: *This process will wipe your data, backup anything important*

**It may cause a brick if done incorrectly.**

I am **not responsible** for any damage caused.

1. Enable *Developer mode*

   Settings > About device > Version > Version No.
3. Enable *USB Debugging* and *OEM Unlocking*
4. Install `android-tools` on your PC
5. Connect your phone to your PC via USB
6. On your PC, open Terminal and run
   ```bash
   adb reboot bootloader
   ```
If there's any prompt that asks if you trust the device for USB debugging, click on always trust and *Accept*

6.5. On your PC, run
   ```bash
   fastboot devices
   ```
If there's no output, look in Device Manager for your phone, if it's not there, your PC isn't detecting the phone

7. If there IS output, run this
   ```bash
   fastboot flashing unlock
   ```
Press **Volume Up** on your phone to Accept

This will wipe your phone.

8. Reboot into your normal phone and go to *Developer options*, *OEM Unlocking* should be greyed out now
   ```bash
   fastboot reboot
   ```
9. Install your root manager (Magisk, KernelSU, ...)
10. Reboot into fastboot again
    ```bash
    adb reboot bootloader
    ```
11. Run this
    ```bash
    fastboot flash init_boot "path/to/file.img"
    ```
12. Reboot into your phone and verify root
