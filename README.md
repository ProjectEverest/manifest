# This is ProjectEverest [EverestOS]

# Build guide

Prior to building, you will need basic knowledge of [Git](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).

### Requirements
- Around 350GB Disk Space.
- A computer with at least 32GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts).

# Getting Started

### Initialize local repository

```
repo init -u https://github.com/ProjectEverest/manifest -b 14 --git-lfs
```

### Sync up 

```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

# Inherit the vendor
```
$(call inherit-product, vendor/lineage/config/common_full_phone.mk)
```
# Build Flags
```
# Maintainer name for Everest

EVEREST_MAINTAINER := "XYZ"

# Adding Blur support

TARGET_SUPPORTS_BLUR := true

# For UDFPS devices

TARGET_HAS_UDFPS := true

EXTRA_UDFPS_ANIMATIONS := true

# Build GAPPS\Vanilla

WITH_GAPPS := true\false

# Quick switch (add more than one Launcher in build)

TARGET_PREBUILT_LAWNCHAIR_LAUNCHER := true

TARGET_DEFAULT_PIXEL_LAUNCHER := true
```

# Build

```
. build/envsetup.sh
```
---
```
lunch lineage_<devicecodename>-user
```
---
```
mka everest -j$(nproc --all)
```

### Compilation Help
To get help with build errors, please visit [**Android Building Help**](https://t.me/AndroidBuildingHelp).

## Credits
 * [**LineageOS**](https://github.com/LineageOS)
 * [**The Parasite Project**](https://github.com/TheParasiteProject)
 * [**Project Awaken**](https://github.com/Project-Awaken)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**Yet another AOSP project**](https://github.com/Yaap)
 * [**crDroid**](https://github.com/crdroidandroid)
