# This is ProjectEverest [EverestOS]

# Build guide

Prior to building, you will need basic knowledge of [Git](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).

### Requirements
- Around 100G disk space.
- A computer with at least 16GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts).

### Instructions
1. Run the following commands to sync source

```
repo init -u https://github.com/ProjectEverest/android_manifest -b udc
```
2. To sync source, enter

```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

3. Once the source is downloaded/synced, prepare your device trees, dependencies and start the build by the following commands

```
   source build/envsetup.sh
   lunch everest_<devicecodename>-user
   make bacon -j$(nproc --all)
```

### Compilation Help
To get help with build errors, please visit [**Android Building Help**](https://t.me/AndroidBuildingHelp).

## Credits

 * [**LineageOS**](https://github.com/LineageOS)
 * [**CodeAurora Forum**](https://source.codeaurora.org/quic/la)
 * [**ArrowOS**](https://github.com/ArrowOS)
 * [**SuperiorOS**](https://github.com/superioros)
 * [**Project Awaken**](https://github.com/Project-Awaken)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**Syberia Project**](https://github.com/syberia-project)
 * [**Yet another AOSP project**](https://github.com/Yaap)
 * [**Pixel OS**](https://github.com/pixelos-aosp)
 * [**ProjectBlaze**](https://github.com/ProjectBlaze)
