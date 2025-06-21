# Hackintosh EFI for [ASUS ROG STRIX G531GD] - macOS Sonoma

This is a complete EFI configuration for running **macOS 14 Sonoma** on a `[ASUS ROG STRIX G531GD]` setup.
-----

## 📋 Hardware Specifications

This EFI is specifically tailored for the following hardware. It may not work on different components without modification.

| Component         | Model                                   |
| ----------------- | --------------------------------------- |
| **CPU** | `[I5-9300H]`          |
| **GPU** | `[GTX 1050 Mobile - 4GB]`            |
| **RAM** | `[16GB DDR4 2666MHz]`            |
| **Storage** | `[Micron 2200V - 512GB NVMe SSD]`               |
| **Ethernet** | `[Realtek PCle GBe]`                 |
| **Wi-Fi/Bluetooth** | `[Intel Wireless-AC9560 160MHz]`        |
| **Audio Codec** | `[Realtek ALC1200]`              |
| **OpenCore Version**| `[1.0.0]`                        |

-----

## What's not Working?

  - [x] **Graphics Acceleration (QE/CI)**
  - [x] **Sleep / Wake**
  - [x] **AirDrop, Handoff, Continuity**
  - [x] **Micron 2200V NVME SSD**

-----

## ⚙️ Installation

1.  Create a macOS Sonoma installer USB using the [Dortania guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/).
2.  Download or clone this repository.
3.  Mount the USB's EFI partition.
4.  Copy the **EFI** folder from this repository to the USB's EFI partition.
5.  **IMPORTANT:** You **MUST** generate your own unique SMBIOS (Serial Number, MLB, SystemUUID) using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS). Never use the SMBIOS from the sample config file, as it can get your Apple ID banned.
      * Model to generate: `[e.g., iMac20,1]`
6.  Configure your BIOS according to the Dortania guide [here](https://www.google.com/search?q=https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html%23intel-bios-settings). (Make sure to select the guide for your specific CPU generation).
7.  Boot from the USB and proceed with the macOS installation.

### Post-Install

  * Mount the EFI partition of the drive where macOS is installed.
  * Copy the EFI folder from the USB to the main drive's EFI partition.

-----

## ⚠️ Disclaimer

This EFI is provided as-is. I am not responsible for any damage, data loss, or other issues that may arise from using it. Please proceed at your own risk and always back up your important data.

This project is for educational and research purposes only.

## 🙏 Credits

  * **[Acidanthera](https://github.com/acidanthera)** for OpenCore and many essential kexts.
  * **[Dortania](https://dortania.github.io/)** for the comprehensive OpenCore Install Guide.
