# MG4 Headunit UI Mod

![IMG_7242](https://github.com/user-attachments/assets/ee0e91c5-dc21-40ee-a962-243529e91b5c)

**A project to port newer MG vehicle UI features to the legacy MG4 infotainment system.**

## Installation methods

**Manual**
1. Download the APK and copy it to a FAT32 formatted USB drive. 
2. Install the APK via the Android system menu using the Files app.

**Automatic**
Coming soon

**Deinstall**
For deinstall, simply open Android settings, go to installed apps and select launcher. Tab on the three dots > deinstall.

## What works after patching

✅ AS33 launcher UI loads on EH32 hardware

✅ All widgets, cards and icons loads correctly

## Known limitations / open issues

⚠️ Widget tiles are not yet correctly sized for the EH32 display resolution

⚠️ No batterycard anymore

⚠️ For now i only patched the launcher.apk to AS33

## ToDo's

✍️ Patch more APK's to AS33 for full infotainemnt menu

✍️ Add different installation method via usb upgrade from the engineering menu

✍️ Find MG4 (Urban), MGS5, MGS6... FCIM for the latest car model infotainment UI

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

