# ThinkPad P15 Gen 1 – OpenCore EFI (macOS Sequoia)

A working [OpenCore](https://github.com/acidanthera/OpenCorePkg) EFI for the **Lenovo ThinkPad P15 Gen 1** (Comet Lake, i7‑10850H).
Tested on **macOS Sequoia 15.8.2** with **OpenCore 1.0.8 (RELEASE build)** and the `MacBookPro16,1` SMBIOS.

> **Generate your own SMBIOS before booting.** The serial, MLB, ROM and UUID in `config.plist` are intentionally blank. Fill in `PlatformInfo → Generic` with your own values (for example from `macserial` or [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)) and don't publish them.

> Hackintoshing is not supported by Apple and goes against Apple's license terms for non‑Apple hardware. This EFI is provided **as is, with no warranty**. Back up your data and keep a copy of your working EFI before changing anything.

## Tested hardware

| Part | Details |
| --- | --- |
| Laptop | Lenovo ThinkPad P15 Gen 1 |
| CPU | Intel Core i7‑10850H (Comet Lake) |
| iGPU | Intel UHD Graphics 630 (used by macOS) |
| dGPU | NVIDIA Quadro T2000 – **disabled in macOS** (unsupported) |
| RAM | 32 GB DDR4 |
| Ethernet | Intel I219 |

## Status

| Feature | Status | Notes |
| --- | --- | --- |
| Boot / install / system updates | ✅ | |
| Intel UHD 630 graphics, display | ✅ | |
| Battery status | ✅ | |
| USB ports | ✅ | |
| Ethernet (I219) | ✅ | |
| Wi‑Fi (Intel) | ✅ | Needs the [HeliPort](https://github.com/OpenIntelWireless/HeliPort) app to connect |
| Audio | ✅ | Vocals can sound faint on headphones; turning on Mono audio in Accessibility fixes it |
| Sleep / wake | ⚠️ | Not fully stable |
| Bluetooth | ❌ | Unreliable |
| NVIDIA Quadro T2000 | ❌ | Switched off in macOS on purpose |

## Credits

- [Acidanthera](https://github.com/acidanthera) – OpenCore, Lilu, VirtualSMC, WhateverGreen, AppleALC, NVMeFix, CPUFriend, IntelMausi, VoodooPS2, ECEnabler (1Revenger1), BlueToolFixup
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) – the OpenCore install guide and prebuilt SSDT references
- [OpenIntelWireless](https://github.com/OpenIntelWireless) – itlwm, HeliPort, IntelBluetoothFirmware
- RehabMan – ACPIBatteryManager, VoodooTSCSync, ACPIDebug; lvs1974 – HibernationFixup, RTCMemoryFixup, CpuTscSync
- daliansky – `SSDT-PNLF_CoffeeLake`
- [USBToolBox](https://github.com/USBToolBox) – USB mapping

Each kext and tool keeps its own license; check the upstream projects before redistributing.
