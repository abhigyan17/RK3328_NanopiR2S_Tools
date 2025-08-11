 NanoPi R2S Toolbox & Firmware Repository

Welcome to the NanoPi R2S All-in-One Toolkit! This repository provides everything you need for development, recovery, and firmware customization for the NanoPi R2S and NanoPi R2S Plus—including the official Rockchip RK3328 SDK, essential flashing utilities, and a curated, regularly updated collection of fully compatible firmware images (OpenWrt, FriendlyWrt, etc.).



 📦 Repository Contents

- SDK & Build Tools
  - Official and community Rockchip RK3328 SDK
  - Board-specific build scripts and environment setup guides

- Firmware Images (Ready-to-Flash)
  - Latest OpenWrt/FriendlyWrt releases (SD/eMMC/USB upgrade images)
  - Community builds and special editions (check `firmware/README.md`)

- Flashing & Recovery Tools
  - eFlasher images for eMMC/SD
  - RKDevTool and USB drivers (for Windows/Linux)
  - Verified partitioned and update.img images for brick recovery

- Useful Scripts
  - Quick start scripts for SSH, network setup, diagnostics, reboot/backup
  - Batch install/upgrade shell scripts for OpenWrt/FriendlyWrt

- Documentation
  - Illustrated, step-by-step guides for every possible scenario



 🚀 Quick Start

Download a Ready Firmware & Flash via SD Card:
1. Get the latest SD card image from the `firmware/` folder.
2. Write the image using [Balena Etcher].
3. Insert SD card → Power on → Login at `192.168.2.1` (default)

![NanoPi R2S flashing with Etcher]



 🛠️ All-in-One Tools: SDK, Recovery, & Utilities

- Build Your Own Firmware
  - In `sdk/`, run `./build.sh` after following the provided config instructions.

- Recover Bricked Devices
  - Use `tools/RKDevTool` for Windows, or eFlasher images for SD bootable restoration.
  - Follow the detailed [recovery guide](docs/RECOVERY.md) with annotated screenshots.

![RKDevTool maskrom flashing workflow]

- Batch Upgrade & Package Installation
  - Use `scripts/batch_upgrade.sh` for CLI mass firmware upgrades.
  - Collection of useful one-liners for package management inside `/scripts`.



 📑 Table of Contents

- [Getting Started](getting-started)
- [Rockchip SDK & Building Firmware](rockchip-sdk--building-firmware)
- [Firmware Selection Guide](firmware-selection-guide)
- [Flashing & Recovery Methods](flashing--recovery-methods)
- [Troubleshooting](troubleshooting)
- [FAQ](faq)
- [Contributing](contributing)



 🏁 Getting Started

 Hardware Required
- NanoPi R2S or R2S Plus
- SD card (≥ 8GB, class 10+)
- USB-C power source (5V/2A recommended)
- Windows/Linux/Mac for flashing utilities



 🔧 Rockchip SDK & Building Firmware

- All SDK sources and required scripts are in `/sdk`
- See [BUILDING.md](sdk/BUILDING.md) for setting up your environment, downloading toolchains, and compiling images for the RK3328 SoC.
- Pre-built community kernels are available in `/builds`



 📥 Firmware Selection Guide

| Firmware Type        | File Format                  | Supported Boards      | Best For                    |
|----------------------|-----------------------------|----------------------|-----------------------------|
| OpenWrt Stable       | `.img.gz` (SD/eMMC)         | R2S, R2S Plus        | Custom router, VPN, advanced |
| FriendlyWrt Official | `.img.gz` / `update.img`    | R2S, R2S Plus        | FriendlyARM optimized, GUI   |
| USB Upgrade Pack     | Partitioned + config        | R2S Plus             | Recovery via RKDevTool      |
| Community Builds     | see `firmware/README.md`    | R2S, R2S Plus        | Tweaks, special configs     |



 💾 Flashing & Recovery Methods

 SD Card / eMMC Flashing

1. Download desired `.img` or `.img.gz` image.
2. Flash with [Balena Etcher] or Win32 Disk Imager.

 USB Maskrom Recovery (Bricked Devices)
1. Enter MaskROM mode with NanoPi R2S Plus (hold MASK button, plug USB-C).
2. Use `tools/RKDevTool`:
   - Select `update.img` (or config for partition set)
   - Click “Upgrade” or “Execute”
3. Wait for completion; remove cable and reboot.

![NanoPi R2S Plus in MaskROM Mode]

> Tip: For easy installation to eMMC, use eFlasher SD images and follow the web GUI instructions.



 📈 Troubleshooting & Tips

- If a flash tool reports "Firmware load failed", check the image type: only `update.img` or partitioned images are valid for RKDevTool.
- SD boot not working? Try another card, re-burn image, or verify power supply.
- For full system backup/restore, use provided scripts in `/backup`.



 💬 FAQ

- Where do I get the latest firmware?  
  See the [firmware/](firmware/) folder, updated monthly.
- Can I build custom packages?  
  Yes! Use the SDK and our helper scripts.
- My device is bricked—what now?  
  Detailed MaskROM + eFlasher recovery steps are in [docs/RECOVERY.md](docs/RECOVERY.md).



 🤝 Contributing

- Pull requests with new tools, fixes, or documentation are welcome!
- Test new firmware on your R2S and report results for future users.



 ❤️ Screenshots



Flashing SD Card with Etcher



MaskROM recovery workflow with RKDevTool



NanoPi R2S Plus in Flashing Mode


Here are the primary links and references you should include in your README for a NanoPi R2S tool and firmware collection. These sources cover official documentation, firmware downloads, SDK/build instructions, and community resources:



 📚 Official Documentation and Product Info

- NanoPi R2S Product Wiki:  
  https://wiki.friendlyelec.com/wiki/index.php/NanoPi_R2S[1]

- NanoPi R2S Plus Product Wiki:  
  https://wiki.friendlyelec.com/wiki/index.php/NanoPi_R2S_Plus[2]

- FriendlyElec Homepage (Product & Specs):  
  https://www.friendlyelec.com[3]



 🖥️ Firmware Downloads

- OpenWrt Official Download Page:  
  https://downloads.openwrt.org[4]
    - [Firmware Selector (find your board & firmware)](https://firmware-selector.openwrt.org)[5]
    - [OpenWrt Supported Devices: NanoPi R2S](https://openwrt.org/toh/friendlyarm/nanopi_r2s)[6]

- OpenWrt Stable Releases (all architectures):  
  https://github.com/openwrt/openwrt/releases[7]

- FriendlyWrt Release (Official Builds):  
  https://github.com/friendlyarm/Actions-FriendlyWrt/releases[8]

- FriendlyWrt Documentation & Build Instructions:  
  https://wiki.friendlyelec.com/wiki/index.php/How_to_Build_FriendlyWrt[9]
  https://wiki.friendlyelec.com/wiki/index.php/FriendlyWrt[10]

- Community NanoPi R2S/R4S Builds:  
  https://github.com/anaelorlinski/OpenWrt-NanoPi-R2S-R4S-Builds[11]



 🔧 Toolkits and SDKs

- Official Rockchip/FriendlyWrt SDK & Build Tooling:  
  See build instructions under “How to Build FriendlyWrt”  
  https://wiki.friendlyelec.com/wiki/index.php/How_to_Build_FriendlyWrt[9]

- Actions-FriendlyWrt GitHub (Source and Actions):  
  https://github.com/friendlyarm/Actions-FriendlyWrt[12]



 💡 Additional References & Useful Pages

- OpenWrt General Overview:  
  https://en.wikipedia.org/wiki/OpenWrt[13]

- Armbian for NanoPi R2S:  
  https://www.armbian.com/nanopi-r2s/[14]

- NanoPi R2S on GitHub (Tags and Variants):  
  https://github.com/topics/nanopi-r2s?o=asc&s=forks[15]



 Example Markdown Snippet for README

```markdown
 References

- [NanoPi R2S Wiki][1]
- [NanoPi R2S Plus Wiki][5]
- [OpenWrt Downloads][6]
- [OpenWrt Firmware Selector][18]
- [FriendlyWrt Official Releases][15]
- [How to Build FriendlyWrt][7]
```

You can embed these links at relevant sections of your README to provide direct download or documentation paths for users. This will help make your repository both comprehensive and authoritative for NanoPi R2S users and enthusiasts.

If you need direct, step-specific links for particular firmware releases or tools (e.g., direct SD/eMMC image paths, SDK tarballs, flashing utilities), let me know!

[1] https://wiki.friendlyelec.com/wiki/index.php/NanoPi_R2S
[2] https://wiki.friendlyelec.com/wiki/index.php/NanoPi_R2S_Plus
[3] https://www.friendlyelec.com
[4] https://downloads.openwrt.org
[5] https://firmware-selector.openwrt.org
[6] https://openwrt.org/toh/friendlyarm/nanopi_r2s
[7] https://github.com/openwrt/openwrt/releases
[8] https://github.com/friendlyarm/Actions-FriendlyWrt/releases
[9] https://wiki.friendlyelec.com/wiki/index.php/How_to_Build_FriendlyWrt
[10] https://wiki.friendlyelec.com/wiki/index.php/FriendlyWrt
[11] https://github.com/anaelorlinski/OpenWrt-NanoPi-R2S-R4S-Builds
[12] https://github.com/friendlyarm/Actions-FriendlyWrt
[13] https://en.wikipedia.org/wiki/OpenWrt
[14] https://www.armbian.com/nanopi-r2s/
[15] https://github.com/topics/nanopi-r2s?o=asc&s=forks
[16] https://robu.in/product/nanopi-r2s/
[17] https://github.com/friendlyarm/Actions-FriendlyWrt/pulls
[18] https://github.com/friendlyarm/Actions-FriendlyWrt/blob/master/README_en.md
[19] https://github.com/friendlyarm/friendlywrt/releases
[20] https://github.com/friendlyarm/Actions-FriendlyWrt/actions



 License

All scripts and community guides are MIT. SDK and firmware images follow their respective upstream licenses.



Clone, flash, build, and enjoy advanced control of your NanoPi R2S!