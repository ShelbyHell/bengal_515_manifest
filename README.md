# Sync

```
repo init -u https://github.com/ShelbyHell/bengal_515_manifest -b AU_LINUX_KERNEL.PLATFORM.2.0.R1.00.00.00.004.199 -g default,-mips,-darwin,-notdefault
```

```
repo sync -c -j$(nproc --all) --current-branch --no-clone-bundle --no-tags --force-sync
```