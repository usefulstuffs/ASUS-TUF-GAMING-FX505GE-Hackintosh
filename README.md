<a href="https://www.asus.com/it/supportonly/fx505ge/helpdesk_knowledge/"><img src="https://github.com/usefulstuffs/ASUS-TUF-GAMING-FX505GE-Hackintosh/blob/main/66936053_8228631142.jpg?raw=true" width="30%" height="30%"></a>

# ASUS TUF GAMING FX505GE Hackintosh
Install macOS 13 Ventura on ASUS TUF GAMING FX505GE

## Disclaimer
This repository has the purpouse to only share my hackintosh (OpenCore) configuration and maybe help you hackintosh this laptop.
I don't guarantee it will work for you as hardware might differ.
I WILL TAKE NO RESPONSIBILITY FOR ANY DAMAGE. IF YOU MESS THING UP I WILL LAUGH AT YOU!

## Hackintoshing the laptop
<details>
  <summary><strong> GETTING STARTED </strong></summary>
  <br>
  
  > ### Windows
  1. Download the [EFI](https://github.com/usefulstuffs/ASUS-TUF-GAMING-FX505GE-Hackintosh/releases) from this repository
  2. Download [MacRecovery for Windows](https://github.com/usefulstuffs/macrecovery.exe/releases/latest/download/macrecovery.exe)
  3. Take an USB with atleast 4 GB and completely format it with rufus (filesystem must be FAT32 or Large FAT32).
  4. Copy the EFI folder from the zip you have downloaded.
  5. Now go to the downloads and open a command prompt here.
  6. Run the command ``macrecovery.exe -b Mac-B4831CEBD52A0C4C -m 00000000000000000 download`` to download the recovery of macOS Ventura
  7. When it finishes, copy the ``com.apple.recovery.boot`` to the root of the USB.
  8. The root of the USB should now have 2 folders: ``com.apple.recovery.boot`` and ``EFI``
  9. Now you might want to generate a serial for your "Fake Mac", for this use the [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) tool.
  10. Now reboot and spam esc until you see the boot menu.
  11. Select with the arrow keys your USB, then select again the name of the USB.
  12. If you get to the language picker, congrats! You have booted successfully macOS. Now the install is like a real Mac.
  13. Select disk utility and erase ENTIRELY your disk by enabling all volumes
  14. Give it a name, personally I reccommend "Macintosh SSD"
  15. Once it's done, close disk utility
  16. Connect to Wi-Fi or connect via Ethernet
  17. Select install macOS Ventura
  18. Hit next and agree the license agreement
  19. Select your disk and wait until it installs
  20. You should now get the macOS configuration, complete it.
  21. Now you need to mount the EFI partition or else you can't boot macOS without the USB. You'll use [MountEFI](https://github.com/corpnewt/MountEFI).
  22. Now copy the EFI golder from the USB to the EFI partition you see in finder and you can finally disconnect the USB.
  23. Eject also the EFI partition to unmount it
  24. Enjoy.
> ### Linux
Guide is coming soon.
</details>

<details>
  <summary><strong> MULTIBOOTING </strong></summary>

  If you want to multiboot MacOS with other OS, follow the [dedicated OpenCore guide](https://dortania.github.io/OpenCore-Multiboot/). If you want to use BootCamp for dualbooting MacOS and Windows, follow the instructions on [this page](https://dortania.github.io/OpenCore-Post-Install/multiboot/bootcamp.html).
</details>

<details>
<summary><strong> SOFTWARE </strong></summary>
  
| | Version |
| ---: | :--- |
| ``OpenCore`` | 0.9.7 (RELEASE) |
| ``Ventura`` | 13 |
| ``SMBIOS`` | MacBookPro15,3 |

</details>

<details>
<summary><strong> HARDWARE </strong></summary>
  
| | Device | macOS 13 Ventura compatibility |
| ---: | :--- | :--- |
| ``Chipset`` | Mobile Intel Chipset | No issues |
| ``CPU`` | Intel Core i7-8750H processor, 6 Cores / 12 Threads, 2.2GHz / 4.1GHz, 9MB Cache | No issues |
| ``Memory`` | 16GB dual-channel DDR4-2667MHz, up to 64GB | No issues |
| ``iGPU`` | Intel UHD Graphics 630 | No issues |
| ``dGPU`` | NVIDIA GeForce GTX 1050 Ti (4GB GDDR5 VRAM) | NVIDIA Drivers absent for Ventura. ACPI should be patched to disable dGPU |
| | HDMI 2.0B | HDMI connected directly to NVIDIA GPU and will not work in macOS |
| ``Storage`` | WDC PC SN520 SDAPNUW-256G-1002 | No issues  |
| ``Screen`` | 15.6" Full HD 60Hz, 1920 x 1080 IPS |  No issues |
| ``Webcam`` | Built-in IR HD webcam (1MP / 720P) |  No issues |
| ``WiFi`` | Intel(R) Wireless-AC 9462 | No issues |
| ``Input & Output`` | USB 3.1 Gen 1 (USB-A) x3 | No issues |
| ``Soundboard`` | Realtek ALC235 | No issues |
| ``Battery`` | 4 Cells, 48Whr | About 3-5h after proper Power Management configuration. |
| ``Keyboard`` | Backlight Keyboard Multicolor | After waking up from sleep backlights are not working. |
| ``Touchpad`` | ELAN1200 Touchpad | Not working for now. Please use an [USB mouse](https://www.amazon.com/s?k=usb+mouse). |

</details>

<details>
  <summary><strong> TROUBLESHOOTING </strong></summary>
  
  * Use [Google](https://google.com) or [Bing](https://bing.com) or whatever search engine to search for problem fixes.
  * Check [OpenCore Forums](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/FORUMS.md) also for problem fixes and for known issues.
</details>

<details>
<summary><strong> CREDITS </strong></summary>
  
* [Dortania](https://dortania.github.io/) - for Vanilla guides
* [Acidanthera](https://github.com/acidanthera) - for OpenCore and lots of kexts
* [RehabMan](https://github.com/RehabMan) - for ACPI patching guides
</details>
