# thinkpad-e480-hackintosh-monterey
Hackintosh macOS Big Sur &amp; Monterey on ThinkPad E480
`OpenCore 0.7.5`

Tested on:

- 11.~ Big Sur
- 12.~ Monterey

## Disclaimer

I am not responsible for any loss, including but not limited to Kernel Panic, device fail to boot or can not function normally, storage damage or data loss, and so on.

## Devices

| Specifications | Details |
|:---|:---|
| Computer Model | ThinkPad E480 (2018) |
| CPU | Intel Core i5-8250U |
| Memory | DDR4 2400 Mhz. Manually upgrade to 2x16 GB |
| NVMe SSD | - |
| SATA SSD | Manually change to Samsung SSD 860 EVO 1 TB |
| Integrated Graphics | Intel UHD Graphics 620 |
| Ethernet | RTL8168/8111/8112 Gigabit Ethernet Controller |
| Sound Card | Conexant CX20753/4 (layout-id: 15) |
| Wireless Card | Manually change to BCM94352Z (DM1560) |

## What is working

#### CPU

XCPM power management is native supported. HWP is fully enabled as well.

#### Battery

The power display is functioning normally.

#### Wi-Fi

The OEM wireless model is `Realtek 8821CE Wireless LAN 802.11ac PCI-E NIC`. Suggest replacing it with BCM94352Z (DM1560).

#### USB

USB Ports Patching with HackinTool, `5 Gbps` for USB 3.0 (Dev Speed).

#### Ethernet

Functioning normally.

#### Display

The model of Integrated Graphics is `Intel UHD Graphics 620`, faked to `Intel HD Graphics 620`. VRAM has been set to 3072 MB.

The HDMI is attached with `Intel UHD Graphics 620` and is functioning normally. `2K@60Hz` & `4K@30Hz` are supported.

#### Audio

Driven by AppleALC with `layout-id: 15`. Everything is working normally.

#### Keyboard

Functioning normally except the <kbd>Insert</kbd> key, which is not presented on Magic Keyboard. Keyboard backlight is working properly as well.

#### SSD

Both NVMe & SATA are functioning normally and TRIM is enabled for both of them.

#### Bluetooth, Handoff, Airplay, Airdrop

Functioning normally, but Airdrop only from iPhone to MacOS. 

#### Trackpad & Trackpoint

Functioning normally. Trackpoint and UltraNavs are working properly as well.

## What is not working

<kbd>Fn</kbd> shortcut might stop working after wake from sleep. It is a common bug happened among ThinkPad E470, E480 E490, E570, E580, E590, etc.

## Recommended BIOS Config

> Make sure you have disabled Windows login password before entering the BIOS, because you might not be able to login with "PIN" on Windows after configuring your BIOS as following.

- Security
  - Intel SGX: Disabled
- Boot
  - Boot Mode: Both UEFI and Legacy
  - Boot Priority: UEFI First
  - Quick Boot: Enabled

## Tips

### Hibernation

Hibernation is supported.

### Known Issue

- After waking up from sleep, there may be a problem that the battery does not quickly update after plugging in and unplugging the power supply. The temporary solution is to manually sleep the system again, and it will return to normal after waking up. <br>
- Bluetooth headphone (Ex. Airpods) sometimes disconnect/unstable connection if the distance is far (> 3 meters). <br>
- Airdrop only from iPhone to MacOS. 
These problems are being solved.



## Big Thanks

**(Original) ThinkPad E480 Hackintosh** [Sukka](https://github.com/SukkaW).
