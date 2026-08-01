# Info

Discord - valenvnovel 

Contains patched *init_boot* images for many root solutions

Also contains stock *init_boot.img* and *boot.img* for APatch users (see the APatch guide)

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

$${\color{red}WARNING: This process will wipe your data, backup anything important}$$
$${\color{red}It may cause a brick if done incorrectly.}$$

$${\color{red}I am not responsible for any damage caused}$$

1. Enable *Developer mode*
   Settings > About device > Version > Version No.
2. Enable *USB Debugging* and *OEM Unlocking*
3. Install `android-tools` on your PC
4. Connect your phone to your PC via USB
5. On your PC, open Terminal and run
   ```bash
   adb reboot bootloader
   ```
or
   ```bash
   adb reboot fastboot
   ```
If there's any prompt that asks if you trust the device for USB debugging, click on always trust and *Accept*
6. On your PC, run
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
11. Run this
    ```bash
    fastboot flash init_boot "path/to/file.img"
    ```
12. Reboot into your phone and verify root
