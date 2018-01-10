# MKNTFS binary for Android devices

Prebuilt binaries of `mkntfs` utility from [NTFS-3G](https://www.tuxera.com/community/open-source-ntfs-3g/) sources.
This utility can work with NTFS filesystems on Android devices. 

NTFS-3G version:  **STABLE 2017.3.23 (March 28, 2017)**

# Requirements 
 - Android API >= 21 (may work on API less then 21, but need to be tested)
 - Supported architecture: armeabi-v7a, arm64-v8a, x86, x86_64
 - May not work without root (neede to be tested)

# How to use
 - Copy the binary for the desired architecture to the device (preferably, for example, **/system/bin/**. It may not work from **/sdcard**)
 - Add execution permissions to the file (`chmod a+x mkntfs`)
 - Run `mkntfs --help` in shell on device to get infomation how to use this binary

# Example of usage
Command to create NTFS filesystem on block device (`-f` - Perform a quick format):
```
mkntfs -f /dev/block/sdg1
```
`/dev/block/sdg1` - path to USB flash drive block device connected to my phone via OTG. This path is actual only for my device. This path can be different on other devices.