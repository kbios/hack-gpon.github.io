---
title: Huawei MA5671A
has_children: true
parent: ONT
---

# Hardware Specifications

|             |                                     |
| ----------- | ----------------------------------- |
| Vendor      | Huawei                              |
| Model       | MA5671A                             |
| Chipset     | Lantiq PEB98035                     |
| Flash       | 16 MB                               |
| RAM         | 64 MB                               |
| System      | OpenWRT                             |
| HSGMII      | Yes                                 |
| Optics      | SC/APC                              |
| IP address  | 192.168.1.10                        |
| Web Gui     | After root                          |
| SSH         | ✅ user `root`, password `admin123` |
| Form Factor | miniONT SFP                         |

{% include image.html file="g-s010s-p-and-ma5671a.jpg"  alt="G-010S-P and MA5671A Teardown" caption="G-010S-P and MA5671A Teardown" %}


##  Firmware is interchangeable with:

- [Huawei MA5671A](ont-huawei-ma5671a)
- [Nokia G-010S-P](ont-nokia-g-s010s-p)
- [SourcePhotonics SPS-34-24T-HP-TDFO](ont-SourcePhotonics-SPS-34-24T-HP-TDFO)
- [Hilink HL23446](ont-Hilink-HL23446)
- Dasan H650SFP {: .text-red-200 }
- DpOptics D23446 {: .text-red-200 }

## Serial

```
USB TTL(UART) Adapter ------- SFP 20pins Molex connector
3.3V ---red ------------------pin #15 and #16
TX -----orange ---------------pin #2
RX -----yellow ---------------pin #7
GND ----green --------------- pin #10
```
Configuration: asc0=0 115200 8-N-1

## Root procedure

- [Root](ont-huawei-ma5671a-root)

##  Disabling Dying Gasp
```sh
set nDyingGaspEnable disable
```

## List of software versions

## List of partitions

- mtd2
- mtd5

## List of firmwares and files

- [Carlito MTD2](https://ma5671a.s3.nl-ams.scw.cloud/mtd2.bin){: .btn }  md5hash: d3cb6f7efec201b37931139feb4bb23b
- [Huawei Rooted MTD2](https://ma5671a.s3.nl-ams.scw.cloud/mA5671a_root_mtd2.img){: .btn } md5hash: 3138d2dd06a32bb92bc63610fec6fcd6
- [Carlito MTD5](https://ma5671a.s3.nl-ams.scw.cloud/mtd5.bin){: .btn }  md5hash > 59d2dc15227d6f693a38131eca89b29e 
- [Huawei Rooted MTD5](https://ma5671a.s3.nl-ams.scw.cloud/mA5671a_root_mtd5.img){: .btn }  md5hash: 0e4cfdc1b96be6581869b26b48789556
- [1224abort.bin](https://ma5671a.s3.nl-ams.scw.cloud/1224ABORT.bin){: .btn }  md5hash: 10e94a4b4acdc82dec20c7904b69e5c0

# General setting

## Setting image version
```sh
fw_setenv image0_version V1.7.6-170626
fw_setenv image1_version V1.7.6-170626
```

## Setting S/N
```sh
fw_setenv ont_serial ABCD12345678
```
or
```sh
uci set gpon.ploam.nSerial="0x48 0x57 0x54 0x43 0x9D 0xAC 0xC7 0xA3"
uci commit 
```

## Setting PLOAM Password
```sh
fw_setenv nPassword "0x30 0x31 0x32 0x33 0x34 0x35 0x36 0x37 0x38 0x39"
```
or
```sh
uci set gpon.ploam.nPassword="0x30 0x31 0x32 0x33 0x34 0x35 0x36 0x37 0x38 0x39"
uci commit 
```

## Setting and check oem-generic
```sh
fw_setenv target oem-generic
fw_printenv target=oem-generic
```

## Setting HSMIII
```sh
fw_setenv sgmii_mode 5
```
# Known Bugs

# Miscellaneous Links

- [Support MA5671A SFP GPON - OpenWRT forum](https://forum.openwrt.org/t/support-ma5671a-sfp-gpon/48042)
- [u boot lantiq falcon - GitHub](https://github.com/minhng99/u-boot_lantiq_falcon)
- [Custom Firmware - right.com.cn](https://www.right.com.cn/forum/thread-8220173-1-1.html)
- [Come avere i 2.5 Gbps su un unico dispositivo senza il Fastgate - fibra.click Forum](https://forum.fibra.click/d/17836-come-avere-i-25-gbps-su-un-unico-dispositivo-senza-il-fastgate)
- [GPON SFP Tools](https://github.com/MokkaSchnalle/GPON-SFP-Tools)
- [Come avere i 2.5 Gbps su un unico dispositivo senza il Fastgate](https://forum.fibra.click/d/17836-come-avere-i-25-gbps-su-un-unico-dispositivo-senza-il-fastgate)
- [La fibre Orange à 2Gbps, sur un routeur MikroTik 10Gbps CCR2004, via un ONT SFP+](https://lafibre.info/remplacer-livebox/guide-de-connexion-fibre-directement-sur-un-routeur-voire-meme-en-2gbps/msg832904/#msg832904)
- [Bypassing the HH3K up to 2.5Gbps using a BCM57810S NIC](https://www.dslreports.com/forum/r32230041-Internet-Bypassing-the-HH3K-up-to-2-5Gbps-using-a-BCM57810S-NIC)
- [General setting of lantiq](https://forum.fibra.click/d/23881-ma5671a-e-vodafone-25-gbps/64)
- [Manual and firmware for reflashing of HUAWEI MA5671A SFP module](https://github.com/nikbyte/huawei_ma5671a)
