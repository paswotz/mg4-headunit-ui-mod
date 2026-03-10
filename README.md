# MG4 Headunit UI Mod

Force the newer **MG HS EV (AS33) launcher UI** onto the **MG4 Standard/SE (EH32)** head unit by patching `CarModel` in the launcher APK.

## How it works

SAIC/MG uses a single launcher APK (`com.saicmotor.launcher`) across multiple platforms. At runtime, the app reads a system property (`ro.product.carmode`) to determine which UI variant to load. On the MG4 SE this returns model code `0x45`, which selects the EH32-specific layout. The AS33 (MG HS EV) uses model code `0x881` and gets a visually modern UI with different card layouts and additional features. CarModel location: `smali/saicmotor/carapi/constant/CarModel`.

## Installation method

1. Download the APK and copy it to a FAT32 formatted USB drive. 
2. Install the APK via the Android system menu using the Files app.

For deinstall, simply open Android settings, go to installed apps and select launcher. Tab on the three dots > deinstall.

## Patches applied to `CarModel`

| Method | Original behaviour | Patched to |
|---|---|---|
| `getCarModelByGetProperty()` | reads `ro.product.carmode`, returns `0x45` on EH32 | hardcoded `0x881` (AS33) |
| `isAS33Project()` | compares model against AS33 code list | always `true` |
| `isAS33HMI()` | compares model against AS33 HMI list | always `true` |
| `isAS33HevProject()` | checks for AS33 HEV variant | always `false` |
| `isAS33PProject()` | checks for AS33 Plus variant | always `false` |
| `isEh32Project()` | checks for `0x45` | always `false` |
| `isEh32EUUKProject()` | checks for `0x45` + EU region | always `false` |
| `isEh32euuk()` | checks for `0x45` + region | always `false` |
| `isEh32euukMce24Cr()` | checks for `0x45` + year variants | always `false` |
| `isEh32Aus()` | checks for `0x45` + AU market | always `false` |
| `isEh32Israel()` | checks for `0x45` + IL market | always `false` |
| `isAS28Project()` | checks for `0xab`/`0xac` | always `false` |
| `isAS32Project()` | checks for `0xaf`/`0xae` | always `false` |
| `isIP42Project()` | checks for `0x84` | always `false` |
| `isIS31Project()` | checks for IS31 codes | always `false` |
| `isUseHardKeyApp()` | checks for platforms with hardware key service | always `false` (EH32 lacks AS33 HardKeyService) |

## What works after patching

✅ AS33 launcher UI loads on EH32 hardware

✅ All widgets, cards and icons loads correctly

## Known limitations / open issues

⚠️ Widget tiles are not yet correctly sized for the EH32 display resolution

⚠️ No batterycard anymore

⚠️ For now i only patched the launcher.apk to AS33

## ToDo's

✍️ Patch more APK's to AS33 for full infotainemnt menu

✍️ Add different installation method via usb upgrade in the engineering menu

✍️ Find MG4 (Urban), MGS5, MGS6... FCIM for the latest car model infotainment UI

## Target hardware

| Field | Value |
|---|---|
| Vehicle | MG4 Standard MY23 |
| Platform | EH32 |
| Model code | `0x45` (original) → `0x881` (patched) |
| Region | EU |
| Launcher APK | `com.saicmotor.launcher` |

## Disclaimer

This is a reverse-engineering project for personal/educational use on privately owned hardware. Modifying system APKs may void your warranty and could affect vehicle software update compatibility. Use at your own risk.

