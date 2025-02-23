DerpFest Manifests
===================

Getting Started
---------------

To get started with Android, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).
To set up your build environment and sync DerpFest, please follow this guide: [Link](https://raw.githubusercontent.com/nathanchance/android-tools/main/guides/building_aosp.txt)

To initialize your local repository using the AOSP/CAF based DerpFest source, use a command like this:
```bash
repo init --depth=1 -u https://github.com/DerpFest-AOSP/manifest.git -b 15 --git-lfs
```

Clone this repository in `.repo/local_manifests`:
```bash
git clone --single-branch -b derp-15 https://github.com/Atiga-Stuff/local_manifests.git .repo/local_manifests
```

Then to sync up:
```bash
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j8
```
