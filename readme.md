Created this Opencore config and got my Z400 to install and boot macOS Catalina.

Can't guarantee anything, especially for Nvidia GPUs. I used an AMD RX470 and it worked fine.

**ATTENTION, IT WON'T WORK IF YOU DON'T FOLLOW THESE STEPS:**
Use corpnewt's GenSMBIOS to generate the serial numbers for your machine, use iMac 19,1. Paste all info in the plist file. Also, set Generic -> ROM to your machine's MAC address.
You'll find infos to each step here, including editing the EFI/OC/config.plist file: https://dortania.github.io/OpenCore-Install-Guide/config-HEDT/nehalem.html#starting-point

**Be sure your SATA devices are set to ACPI+RAID in the BIOS, disable VTd and enable VTx**

Hope it helps!

**Working:**
- GPU acceleration
- GPU HDMI out
- USB2 ports (even on the card reader)
- SATA devices
- Firewire
- Running very stable

**Not working:**

- Standby
- No audio from on-board sound card (is probably easy to patch)
- GPU DVI out
- Machine keeps running with no display output when macOS tries to restart (just shut the machine down manually)

**Unknown (didn't need any of it so untested):**

- iServices
- DRM video

**My system specs**

- Hardware: HP Z400 Workstation
- CPU: Intel Xeon W3565 3.2GHz Quadcore (Bloomfield / Nehalem)
- GPU: AMD RX470
- RAM: 8GB DDR3 ECC Unbuffered 1333MHz
- Motherboard: Proprietary HP 0B4Ch (X58 Chipset)
- Audio Codec: Apple ALC
- Ethernet Card: Broadcom NetXtreme Gigabit
- Wifi/BT-Card: None

Opencore Version: 0.7.2 Debug
