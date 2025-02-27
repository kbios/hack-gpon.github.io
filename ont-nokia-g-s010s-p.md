---
title: Nokia G-010S-P
has_children: false
parent: ONT
---

# Hardware Specifications

|             |                                                                  |
| ----------- | ---------------------------------------------------------------- |
| Vendor      | Nokia                                                            |
| Model       | G-010S-P                                                         |
| Chipset     | Lantiq PEB98035                                                  |
| Flash       | 16 MB                                                            |
| RAM         | 64 MB                                                            |
| System      | OpenWRT                                                          |
| HSGMII      | Yes                                                              |
| Optics      | SC/APC                                                           |
| IP address  |                                                                  |
| Web Gui     | ✅ [after enabling](https://www.dslreports.com/forum/r32458588-) |
| SSH         | ✅ user `ONTUSER`, password `SUGAR2A041`                         |
| Form Factor | miniONT SFP                                                      |

{% include image.html file="g-s010s-p.jpg"  alt="G-010S-P" caption="G-010S-P" %}
{% include image.html file="g-s010s-p-and-ma5671a.jpg"  alt="G-010S-P and MA5671A Teardown" caption="G-010S-P and MA5671A Teardown" %}

## Firmware is interchangeable with:
- [Huawei MA5671A](ont-huawei-ma5671a)
- [Nokia G-010S-P](ont-nokia-g-s010s-p)
- [SourcePhotonics SPS-34-24T-HP-TDFO](ont-SourcePhotonics-SPS-34-24T-HP-TDFO)
- [Hilink HL23446](ont-Hilink-HL23446)
- Dasan H650SFP {: .text-red-200 }
- DpOptics D23446 {: .text-red-200 }

Turning a [Nokia G-010S-P](ont-nokia-g-s010s-p) into a [Nokia G-010S-A](ont-nokia-g-s010s-A) is possible by changing layout from mtd

## Serial

```
USB TTL(UART) Adapter ------- SFP 20pins Molex connector
3.3V ---red ------------------pin #15 and #16
TX -----orange ---------------pin #2
RX -----yellow ---------------pin #7
GND ----green --------------- pin #10
```
Configuration: asc0=0 115200 8-N-1

## List of software versions
## List of partitions
## List of firmwares and files

##  Disabling Dying Gasp
```sh
fw_setenv nDyingGaspEnable 0
```

# Known Bugs
# Miscellaneous Links

- [alcatel_lucent-lantiq_falcon](https://github.com/minhng99/alcatel_lucent-lantiq_falcon)
- [uboot lantiq falcon](https://github.com/minhng99/u-boot_lantiq_falcon)


