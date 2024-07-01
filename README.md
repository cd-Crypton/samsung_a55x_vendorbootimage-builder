## Samsung Galaxy A55 5G (TWRP)
```
Device: a55x
Vendor: Samsung
Recovery: recovery-as-vendor_boot (vendor_ramdisk_recovery)
```
Workflows Process:
1. This github action compile a vendor_boot image using TWRP source and [a55x-twrp-tree](https://github.com/TheNoobDevs/android_device_samsung_a55x).
2. This will unpack both vendor_boot image from TWRP's $OUT folder and stock vendor_boot image using magiskboot.
3. This will copy the vendor_ramdisk_recovery.cpio of vendor_boot image from TWRP and replace vendor_ramdisk_recovery.cpio of stock vendor_boot image.
4. This will repack the stock vendor_boot image that has new vendor_ramdisk_recovery.cpio and upload as .tar archive for ODIN flashing.
