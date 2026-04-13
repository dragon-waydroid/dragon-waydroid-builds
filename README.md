# Waydroid_arm64 for Qualcomm mainline Linux devices
Add support for HEVC/AVC/VP9 hardware decoding via v4l2_codec2 on Qualcomm mainline Linux devices with the Venus driver.  
Verified on Radxa Dragon Q6A(QCS6490) and Huawei MateBook E Go(SC8280XP).

**Note: This is an experimental release for testing purposes only!**

## How to build

```
repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --git-lfs --depth=1
repo sync build/make

wget -O - https://raw.githubusercontent.com/dragon-waydroid/android_vendor_waydroid/lineage-23.2/manifest_scripts/generate-manifest.sh | bash
repo sync

. build/envsetup.sh
apply-waydroid-patches

. build/envsetup.sh
breakfast waydroid_arm64
make systemimage vendorimage -j$(nproc --all)
```

## References
- [WayDroid-ATV](https://github.com/WayDroid-ATV)
- [raspberry-vanilla](https://github.com/raspberry-vanilla)
- [Waydroid Docs](https://docs.waydro.id/development/compile-waydroid-lineage-os-based-images)
- [LineageOS Wiki](https://wiki.lineageos.org/)
