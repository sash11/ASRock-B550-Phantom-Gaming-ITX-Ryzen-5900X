# ASRock-B550-Phantom-Gaming-ITX-Ryzen-5900X
 <p align="center">
  <img src="Docs/AboutMac.png" align=center">
 </p>
 <p align="center">
  <img src="Docs/PCI.png" align=center">
 </p>
  <p align="center">
  <img src="Docs/Geekbench.png" align=center">
 </p>
   <p align="center">
  <img src="Docs/CinebenchMulti.png" align=center">
 </p>

 ## Specs
| **Component** | **Model** |
| ------------- | --------- |
| CPU | Ryzen 9 5900X |
| RAM | DDR4 64GB (2x32GB) 3600MHz |
| Audio Chipset | Realtek ALC1220. Works with layout-id 1 |
| dGPU | Sapphire RX550 2GB Lexa core. Works with device-id swap |
| WiFi & Bluetooth | BCM94360NG Works OOB. Fits into original Intel card slot |
| Lan |  Intel® 2.5GbE LAN I225-V. Currenly not working |
| OS Disk | 512GB Samsung 970 Pro NVMe |
| macOS | Big Sur 11.4/OpenCore 0.7.0 |

## BIOS
| **Setting** | **Value** |
| ------------- | --------- |
| Above 4G memory | Enabled |
| SATA Mode | AHCI Mode |
| Fast Boot | Disabled |

## USB config
USB Map was created manually. All ports are working.

## Issues
1. Intel Ethernet I225-V card is not working properly. Changing device-id and using FakePCIID kexts does not work on this board. When ethernet cable is plugged in, APIPA address is assigned and system crashes. Currently I have not found a solution to this problem.
2. Reboot and Shutdown have issues. System shuts down, but when trying to power back up, fans start to spin but system does not post. I have to flip the power switch to make it boot. Reboot does not work as well. Monitor shuts down, but system stays powered on. I have to use the PSU switch again. Tried ACPI quirk FadtEnableReset, but it did not help.
