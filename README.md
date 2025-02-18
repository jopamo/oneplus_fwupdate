# OnePlus Firmware Update Script (`oneplus_fwupdate`)

This script automates the process of downloading, extracting, and flashing the latest vendor firmware and LineageOS partitions to a OnePlus Android device. It ensures that the device is updated to the latest firmware versions from both Oplus archive and LineageOS mirror.

## Prerequisites

- `wget` for downloading files
- `zstd` for extracting `.zst` files
- `adb` and `fastboot` for flashing the device
- A OnePlus device connected via USB with fastboot support

## How it Works

1. **Download Firmware Files**  
   The script downloads the latest firmware components from the Oplus archive and LineageOS mirror. Files are only downloaded if they do not already exist on the system.

2. **Extract Firmware Files**  
   `.zst` files are extracted using the `zstd` tool.

3. **Flash the Device**  
   The script reboots the device into fastboot mode, flashes the firmware partitions (boot-related and other firmware images), and reboots the device into recovery mode once the flashing process is complete.

## Usage

1. Clone or download this repository.
2. Ensure your OnePlus device is connected via USB and in fastboot mode.
3. Run the script with:

   ```bash
   ./oneplus_fwupdate.sh
