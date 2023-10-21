### Hackintosh-Lenovo-V310-14ISK-EFI-OpenCore

A Hackintosh EFI backup and share for Lenovo-V310-14ISK (Open core 0.9.5)

### Lenovo-310-14ISK 

| Laptop Type | Bios Version | Installed macOS | Bootloader |
| ----------- | ----------- | ----------- | ----------- | 
| [Lenovo Ideapad 310 14ISK 80SL](https://detail.zol.com.cn/notebook/index1145655.shtml) | [LENOVO Insyde 0ZCN52WW](https://newsupport.lenovo.com.cn/driveDownloads_detail.html?driveId=71387) (Lastest)| Big Sur 11.7.10 | [OpenCore v0.9.5](https://github.com/acidanthera/OpenCorePkg/releases) |

### My Specifications :

| Type | Spec | Status |
| ----------- | ----------- | ----------- |
| Processor | Intel Core i5 6200U Skylake | Working |
| Chipset | Intel Skylake-U | Working |
| RAM | 4GB DDR4  (2133 Mhz) | Working |
| IGPU | Intel HD Graphics 520 | Working |
| dGPU | AMD | Not Supported |
| Storage | 1x SSD 250GB + 1x  HDD SATA 500GB | Working |
| Wifi | Intel AC 3165 + Bluetooth | Working |
| Ethernet | Realtek RTL8168GU Gigabit Ethernet | Working |
| Touchpad | Synaptic SYN2B58 PS2 Interface | Working |
| Keyboard | PS2 Interface | Working |
| Sound | Conexant , Codec ID= Layout ID=3 | Working |
| Battery | Device=L15C4A02, Manufacturer=CPT-LGS3 11 | Working |
| Webcam | Realtek EasyCamera | Working |
| SD Card Reader | Realtek USB 2.0 Card Reader | Untested |

### System Status :

| Type | Status |
| ----------- | ----------- |
| QE/CI Graphics Intel HD 520 | Working |
| CPU Power Management | Working |
| Restart and Shutdown | Working |
| Sleep | Working |
| Brightness Slider & keys F11 - F12 | Working |
| Battery Precentage | Working |
| Touchpad and Gesture | Working |
| HDMI Display | Working |
| HDMI Audio | Working |
| iService | Not Working |

### Used Kext :

| Kext | Info |
| ----------- | ----------- |
| [Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Kernel extension Arbitrary kext and process patching on macOS |
| [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC Emulator Layer |
| [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | To disable Nvidia discrete GPU and patch framebuffer Intel HD 520 |
| [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Processor Monitoring |
| [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Fan Speed Monitoring |
| [SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Battery Monitoring |
| [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | To Patch on-board sound controllers|
| [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) | To Patch Intel AC 3165 |
| [IntelBluetoothInjector.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | To patch Intel Bluetooth |
| [IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | To patch Intel Bluetooth |
| [IntelBTPatcher.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | To patch Intel Bluetooth |
| [RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | To Patch The Ethernet port |
| [CtlnaAHCIPort.kext](https://github.com/dortania/OpenCore-Install-Guide/blob/master/extra-files/CtlnaAHCIPort.kext.zip) | Adds support for SATA controllers in Big Sur+ |
| [USBToolBox.kext](https://github.com/USBToolBox/tool/releases) | kext for USB port |
| [UTBMap.kext](https://github.com/USBToolBox/tool/releases) | To generate USB map |
| [ECEnabler.kext](https://github.com/1Revenger1/ECEnabler/releases) | To enable Patch battery percentage |
| [VoodooTSCSync.kext](https://github.com/RehabMan/VoodooTSCSync) | A kernel extension which will synchronize the TSC on any Intel CPUs |
| [VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases) | Input driver for laptop |
| VoodooPS2Keyboard.kext | keep it in order in the config.plist |
| VoodooPS2Mouse.kext | keep it in order in the config.plist |
| VoodooPS2Trackpad.kext | keep it in order in the config.plist |
| VoodooInput.kext | keep it in order in the config.plist |
| [BrightnessKeys.kext](https://github.com/acidanthera/BrightnessKeys/releases) | Automatic handling of brightness keys based on ACPI  |

### Used DSDT & SSDT :

| SSDT | Info | Guide |
| ----------- | ----------- | ----------- |
| [SSDT-EC-USBX-LAPTOP.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-LAPTOP.aml) | Used for disabling your real Embedded controller and creating a fake one for macOS to play with. And USBX portion is used for injection USB power properties missing on Skylake and newer | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-prebuilt.html#laptop-skylake-and-kaby-lake) |
| [SSDT-PLUG-DRTNIA.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml) | Used for enabling Apple's XCPM in macOS, allowing for far better CPU power management | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-prebuilt.html#laptop-skylake-and-kaby-lake) |
| [SSDT-PNLF.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml)| Fix Backlight Slider | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html) |
| [SSDT-XOSI](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-XOSI.aml) | Enables many Windows-only functionality in macOS and requires XOSI patch | [Read](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/skylake.html#acpi) |
| [SSDT-HPET.aml](https://dortania.github.io/Getting-Started-With-ACPI/Universal/irq.html)  | Patch IRQ Conflicts | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html#running-ssdttime) |
| [SSDT-SBUS-MCHC.aml](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html) | Fix Intel System Management Bus | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus-methods/manual.html#edits-to-the-sample-ssdt) |

