# TheParasiteProject

## Build Process

### Sync ###

```bash

# Initialize local repository
repo init --depth=1 --no-repo-verify -u https://github.com/angelomds42/TPP-FORK-manifest -b main -g default,-mips,-darwin,-notdefault --git-lfs

# Sync
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosp_$device-userdebug

# Build the code
$ mka bacon -jX
```

## Devices

- [TheParasiteProject-Devices](https://github.com/TheParasiteProject-Devices)
