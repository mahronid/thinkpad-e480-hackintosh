# Hackintosh Thinkpad E480 Ventura (13.4 - OC 0.9.2)

## Table of Contents

- [Hackintosh Thinkpad E480 Ventura (13.4 - OC 0.9.2)](#hackintosh-thinkpad-e480-ventura-134---oc-092)
  - [Table of Contents](#table-of-contents)
  - [Device Information](#device-information)
  - [Usage](#usage)
  - [What-is-working](#what-is-working)
    - [Detailed-Device-Drivers](#detailed-device-drivers)
      - [CPU](#cpu)
      - [Battery](#battery)
      - [USB](#usb)
      - [Ethernet](#ethernet)
      - [Display](#display)
      - [Audio](#audio)
      - [Keyboard](#keyboard)
      - [SSD](#ssd)
      - [Bluetooth](#bluetooth)
      - [Trackpad-Trackpoint](#trackpad-trackpoint)
      - [Wireless-Card](#wireless-card)
      - [Integrated-Camera](#integrated-camera)
      - [Headphone/mic combo](#headphonemic-combo)
  - [What-is-not-working](#what-is-not-working)
    - [Known Issue](#known-issue)
  - [Recommended-BIOS-Config](#recommended-bios-config)
  - [Tips](#tips)
    - [Hibernation](#hibernation)
  - [Support](#support)

## Device Information
| Specifications | Details |
|:---|:---|
| Computer Model | ThinkPad E480 |
| CPU | Intel(R) Core(TM) i5-8250U CPU @ 1.60GHz |
| Model |  Lenevo 20KN|
| Memory | 8 GB ( 2x4 Samsung DDR4 2133 MHz ) |
| NVMe SSD | SSD M.2-SATA SK Hynix HFM128GDHTNG-8510B |
| Integrated Graphics | Intel UHD Graphics 620 (Mobile) |
| Ethernet |  Realtek RTL8168GU/8111GU |
| Sound Card | Conexant CX20753/4 (layout-id: 15) |
| Wireless Card |  Intel(R) Wireless-AC 3165 MHz |


## Usage

If you have the same computer as me, you just need to replace your EFI with the EFI in the current directory. Don't forget to update your serial.

## What-is-working

### Detailed-Device-Drivers

#### CPU

Functioning normally. Patched with CPUFriend.kext: 0.8 GHz (Min) - 3.4 GHz(Max)

#### Battery

The power display is functioning normally.

#### USB

USB Ports Patching with USBMap.kext.

#### Ethernet

Functioning normally.

#### Display

The model of Integrated Graphics is `Intel UHD Graphics 620`, faked to `Intel HD Graphics 620`. VRAM has been set to 3072 MB.

The HDMI is attached with `Intel UHD Graphics 620` and is functioning normally. `2K@60Hz & 4K@30Hz` are supported.

#### Audio

Driven by AppleALC with `layout-id: 15`. Everything is working normally.

#### Keyboard

Functioning normally except the <kbd>Insert</kbd> , which is not presented on Magic Keyboard.

#### SSD

Both NVMe & SATA are functioning normally and TRIM is enabled for both of them.

#### Bluetooth

Bluetooth functioning partially (Failed to connect on iPhone and AirPods)

#### Trackpad-Trackpoint

Functioning normally.

#### Wireless-Card

Functioning normally.

#### Integrated-Camera

Functioning normally.

#### Headphone/mic combo

Functioning normally.


## What-is-not-working

- Airdrops and Handoff Fail to work properly.
- <kbd>Fn</kbd> shortcut might stop working after wake from sleep. It is a common bug happened among ThinkPad E470, E480 E490, E570, E580, E590, etc.

### Known Issue

- After waking up from sleep, there may be a problem that the battery does not quickly update after plugging in and unplugging the power supply. The temporary solution is to manually sleep the system again, and it will return to normal after waking up. <br>
- Bluetooth headphone (Ex. Airpods) sometimes disconnect/unstable connection if the distance is far (> 3 meters). <br>
- Airdrop only from iPhone to MacOS. 
These problems are being solved.

## Recommended-BIOS-Config

- Security
  - Intel SGX: Software Controlled
- Boot
  - Boot Mode: Both UEFI and Legacy (CSM Yes)
  - Boot Priority: UEFI First
  - Quick Boot: Enabled

## Tips

### Hibernation

Hibernation is supported.


## Support

**Ventura**
- 13.4
