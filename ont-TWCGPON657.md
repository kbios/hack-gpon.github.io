---
title: TWCGPON657
has_children: false
parent: ONT
---

# Hardware Specifications

|             |                   |
| ----------- | ----------------- |
| Vendor      |                   |
| Model       | TWCGPON657        |
| Chipset     | Realtek RTL9601CI |
| Flash       | 16 MB             |
| RAM         | 64 MB             |
| System      | Linux (Luna SDK)  |
| HSGMII      | Yes               |
| Optics      | SC/APC            |
| IP address  |                   |
| Web Gui     | ✅                |
| SSH         | ✅                |
| Form Factor | miniONT SFP       |

## Firmware is interchangeable with:

- [VSOL V2801F](ont-vsol-V2801F)
- [TWCGPON657](ont-TWCGPON657)
- [UFiber UF-Instant](ont-UFiber-UF-Instant) 

## List of software versions
## List of partitions
## List of firmwares and files

# Known Bugs

VLAN swap issue (MEID 171), auto-sensing mode to switch between SGMII/HiSGMII

You should use the VID/VLAN shown by executing the command "omcicli mib get 84" via telnet to bring up PPPoE


# Miscellaneous Links

- [Hacking RTL960x](https://github.com/Anime4000/RTL960x)


