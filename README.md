# SOS Android Broken Screen

What if you break the screen of your phone? 
It still works, but it is not usable anymore since the screen is not responding to any command.
This can be annoying if you want to recover your personal data, especially if your device is protected by a code or a visual pattern and if they are on the internal memory of the phone.
Indeed, in that case, when connecting your phone to a computer, the device will not give you access to your data.

However, after some researches, I found a hack to recover your personal data.
This will work only under those conditions:

* Your device is unlocked and rooted
* `adb` and `fastboot` are installed on your computer
* `adb` can detect your device
* A custom recovery is installed

If you haven't installed a custom recovery yet, it can be easily done in the bootloader mode (typically turning on your device using the POWER + VOLUME DOWN buttons) and using

`fastboot flash recovery path/to/your/custom/recovery.img`

## Recover your data

If your device is on, you can reboot your phone into recovery mode using

`adb reboot recovery`

or you can go manually through the bootloader menu.

Then, you can access all data in your phone using

`adb shell`

and find the path of your personal data (often in `/sdcard` folder).
Then, you can transfer files from your phone to your computer using

`adb pull path/to/your/file`
