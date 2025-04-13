# Sync

```
repo init -u https://github.com/ShelbyHell/bengal_515_manifest -b LA.VENDOR.13.2.1.r1-10200-DIVAR.QSSI14.0 -g default,-mips,-darwin,-notdefault
```

```
repo sync -c -j$(nproc --all) --current-branch --no-clone-bundle --no-tags --force-sync
```

# Build only bengal_515
```
 source build/envsetup.sh
 lunch bengal_515-user
 RECOMPILE_KERNEL=1 kernel_platform/build/android/prepare_vendor.sh
 ./build.sh --target_only -j$(nproc --all)
```

# or for build only QSSI
```
    source build/envsetup.sh
    lunch qssi-user
    ./build.sh dist --qssi_only -j "$(nproc --all)"
```

# or full build
```
 source build/envsetup.sh
 lunch bengal_515-user
 RECOMPILE_KERNEL=1 kernel_platform/build/android/prepare_vendor.sh
 ./build.sh -j$(nproc --all)
```