<img src="https://github.com/usefulstuffs/ASUS-TUF-GAMING-FX505GE-Hackintosh/blob/main/66936053_8228631142.jpg?raw=true" width="30%" height="30%">

# ASUS TUF GAMING FX505GE Hackintosh
Install macOS 13 Ventura on ASUS TUF GAMING FX505GE

## Disclaimer
This repository has the purpouse to only share my hackintosh (OpenCore) configuration.
I don't guarantee it will work for you as hardware might differ.
I WILL TAKE NO RESPONSIBILITY FOR ANY DAMAGE. IF YOU MESS THING UP I WILL LAUGH AT YOU!

## Software
| | Version |
| ---: | :--- |
| ``OpenCore`` | 0.9.7 (RELEASE) |
| ``Ventura`` | 13 |

## Hardware
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

## Thanks to...
* [Dortania](https://dortania.github.io/) - for Vanilla guides
* [Acidanthera](https://github.com/acidanthera) - for OpenCore and lots of kexts
* [RehabMan](https://github.com/RehabMan) - for ACPI patching guides

### Where to begin
* Use [Dortania's guide](https://dortania.github.io/OpenCore-Install-Guide) for doing config.plist and create Bootable USB.
* Use [Google](https://google.com) or [Bing](https://bing.com) or whatever search engine to search for problem fixes.
* Check [OpenCore Forums](https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/FORUMS.md) also for problem fixes and for known issues.
