# MG4 Headunit UI Mod

![IMG_7242](https://github.com/user-attachments/assets/ee0e91c5-dc21-40ee-a962-243529e91b5c)

**Upgrade your infotainment system with the latest launcher UI experience from SAIC/MG.**
> [!WARNING]
> Currently, this mod only works with MG4 SE (Standard) models.

## Installation methods
> [!NOTE]
> Choose **Recommended** if you want to install the full base system package.\
> Choose **Manual** if you want to select the modified apps yourself.

**Manual** 

>You already have access to the internal Android system (AAOS) to sideload apk's.
1. Download the latest APK's from [releases](https://github.com/paswotz/mg4-headunit-ui-mod/releases) and copy it to a FAT32 formatted USB drive. 
2. Install the APK's via the Android system menu using the "Files" app.

**Recommend**
> [!IMPORTANT]
> This installation method coming soon.
1. Download the latest "usb_ota_update.zip" from [release](https://github.com/paswotz/mg4-headunit-ui-mod/releases) page.
2. Insert a USB drive (4–32 GB) into your PC and format it as FAT32.
3. Copy the downloaded .zip file directly to the root directory of the USB drive.
4. In the car, connect the USB drive, open the phone dialer and enter `#*#4479*#*`.
5. Select "USB Update". First install "AVN-VIP". After reboot repeat the steps and select "AVN-SOC".

**Deinstallation**
1. Open the android settings and go to the installed apps.
2. Search and select the "launcher" app.
3. Tab on the three dots and select "deinstall".

## Target hardware

| Field | Value |
|---|---|
| Vehicle | MG4 SE MY23 |
| Platform | EH32 |
| Model code | `0x45` (original) → `0x881` (patched) |
| Region | EU |
| Launcher APK | `com.saicmotor.launcher` |

## Disclaimer

This is a reverse-engineering project for personal/educational use on privately owned hardware. Modifying system APKs may void your warranty and could affect vehicle software update compatibility. Use at your own risk.

