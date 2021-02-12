<div align="center">
  
[![](https://img.shields.io/badge/Repositories-basett1-informational?style=flat&logo=apple&logoColor=white&color=9debeb)](https://github.com/basett1?tab=repositories)
[![](https://img.shields.io/badge/Gitter%20Ice%20Lake-Chat-informational?style=flat&logo=gitter&logoColor=white&color=ed1965)](https://gitter.im/ICE-LAKE-HACKINTOSH-DEVELOPMENT/community)
[![](https://img.shields.io/badge/Gitter%20HL%20Community-Chat-informational?style=flat&logo=gitter&logoColor=white&color=ed1965)](https://gitter.im/Hackintosh-Life-IT/community)
[![](https://img.shields.io/badge/Telegram-HackintoshLifeIT-informational?style=flat&logo=telegram&logoColor=white&color=5fb659)](https://t.me/HackintoshLife_it)
[![](https://img.shields.io/badge/Facebook-HackintoshLifeIT-informational?style=flat&logo=facebook&logoColor=white&color=3a4dc9)](https://www.facebook.com/hackintoshlife/)
[![](https://img.shields.io/badge/Instagram-HackintoshLifeIT-informational?style=flat&logo=instagram&logoColor=white&color=8a178a)](https://www.instagram.com/hackintoshlife.it_official/)
[![](https://img.shields.io/badge/PayPal-HackintoshLifeIT-informational?style=flat&logo=paypal&logoColor=white&color=00B2EE)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RWBVVWL8H9JC2&source=url)

</div>



# Asus N551JK OpenCore EFI
Big Sur - Opencore EFI for Asus N551JK 

EFI for ASUS N551JK with OpenCore bootloader 0.6.6

![AsusN551JK](https://user-images.githubusercontent.com/74409308/102687569-4cb7c300-41f0-11eb-9504-3aea777014af.jpg)

# Computer Spec:

| Component        | Brank                              |
| ---------------- | ---------------------------------- |
| CPU              | Intel i7 4710HQ                    |
| iGPU             | Intel® HD Graphics 4600            |
| dGPU             | nVidia GeForce GTX 850M (DISABLED) |
| Lan              | Realtek 8111                       |
| Audio            | Realtek ALC668                     |
| Ram              | 16 GB                              |
| Wifi + Bluetooth | BCM94360HMB                        |
| SmBios           | MacBookPro 11,2                    |
| BootLoader       | OpenCore                           |

# BIOS SETTINGS
# *BIOS VERSION 205*

## Disable cfg lock

To disable cfg lock use the provided kit.

In the folder is provided a dump of BIOS 205 version for references. 

**THANKS TO [LORYS89](https://github.com/Lorys89) for the hints and the kit**

Declare tools in config.plist

Reboot the system, when you are at Opencore run modGRUBShell.efi

Type `setup_var 0x85`to interrogate, the result is `Offset 0x85 is: 0x01` this mean that the cfg lock is enabled

Then type `setup_var 0x85 0x00`to write, the result is `Offset 0x85 is: 0x01 setting offset 0x85 to 0x00` this mean that the cfg lock is disabled

Type `EXIT` to return to Opencore Bootloader, Reset nvram and use VerifyMsrE2.efi to check if the cfg lock is disabled.

## Advanced

Internal pointint device **[ENABLED]**

Wake on lid open **[ENABLED]**

Power off Energy saving **[DISABLED]**


Intel virtualization technology **[ENABLED]**

Intel aes-ni **[ENABLED]**

Vt-d **[DISABLED]**


#### Sata configuration

SATA mode selection **[AHCI]**


#### Graphics configuration

DMVT pre allocated **[128m]**


#### Usb configuration

Legacy USB support **[ENABLED]**

Xhci pre boot mode **[SMART AUTO]**


#### Network stack

Network stack **[DISABLED]**


## Boot

Launch CSM **[ENABLED]**

Launch pxe oprom policy **[ENABLED]**


## Security

Secure boot menu

Secure boot control **[DISABLED]**




# What works and What doesn't or WIP:

- [x] Intel HD GRAPHICS 4600 iGPU
- [x] Intel HD GRAPHICS 4600 iGPU HDMI Output
- [x] Intel HD GRAPHICS 4600 iGPU mDisplayPort Out
- [x] ALC668 Internal Speakers
- [x] ALC668 Internal microphone
- [x] ALC668 Combojack headphones
- [x] ALC668 Combojack microphone
- [x] ALC668 HDMI Audio Output
- [x] ALC668 mDisplayPort Audio Output
- [x] Sleep / Wake also with lid
- [x] PS2 Touchpad with gesture
- [x] Keyboard (PS2-Internal) with backlight
- [x] F3 & F4 Backlight Key
- [x] F5 & F6 Brightness Key
- [x] F10 & F11 & F12 Sound Key
- [x] Wi-Fi and Bluetooth BCM94360HMB Module
- [x] Realtek RTL811 LAN
- [x] Micro SD Cardreader (USB-Internal)
- [x] WebCam (USB-Internal)
- [x] All Sensors CPU, IGPU, BATTERY, FAN
- [x] ACPI Battery
- [x] NVRAM (Native)
- [x] Recovery (macOS) boot from OpenCore
- [ ] Windows 10 boot from OpenCore

# Infos
![Info](https://user-images.githubusercontent.com/74409308/102687566-4aedff80-41f0-11eb-9ef0-f76423aff984.png)
![DPCI MANAGER 1](https://user-images.githubusercontent.com/74409308/102687571-4de8f000-41f0-11eb-8b02-785a2f85ca3a.png)
![DPCI MANAGER 2](https://user-images.githubusercontent.com/74409308/102687573-4f1a1d00-41f0-11eb-93af-a1619c5932c2.png)
- See the [IOREG](https://github.com/basett1/Asus-N551JK-OC-EFI/blob/main/Infos/ANGELO’s%20MacBook%20Pro.ioreg)

# Credits

- [Apple](https://apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and all the lovely hackintosh work.
- [Dortania](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/icelake.html) For great and detailed guides.
- [SPEEEDO83](https://github.com/Speeedo83) For the theme.
- [Hackintoshlifeit](https://github.com/Hackintoshlifeit) Support group for installation and post installation.

# If you need help please contact us on [Telegram](https://t.me/HackintoshLife_it) or [Web](https://www.hackintoshlife.it/)
