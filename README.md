# Krelboyne Go (KrelGo)

A gaming OS for the Lenovo Legion Go, built on Debian 13 (trixie) with live-build. It boots to an Xfce desktop with the dark teal Krelboyne look.

**Status: early work.** The ISO builds and runs in a VM; testing on the Legion Go is next.

Sister project of [KrelboyneOS](https://github.com/grumpy-gaming/KrelboyneOS), which this repo's layout is copied from.

## What's in it

- Steam (Proton comes with Steam Play)
- RetroArch with a starter set of cores, and ES-DE as the game frontend
- Firefox ESR and the Onboard on-screen keyboard
- PipeWire sound, Wi-Fi and firmware

Anything else is opt-in and untested, at your own risk.

## Build it

On a Debian 13 machine with live-build:

    sudo lb clean; lb config; sudo lb build

The ISO, `krelboynego-amd64.hybrid.iso`, appears in the project folder.

## Layout

- `config/includes.chroot/etc/krelgo/branding.conf`: name, version and links, in one place
- `auto/config`: the main live-build settings
- `config/package-lists/`: packages in the image
- `config/hooks/live/`: build scripts (Steam, ES-DE, branding)
- `config/includes.chroot/`: files copied into the image as they are
- `artwork/`: original artwork. The 2560x1600 wallpaper is this image scaled to 1600 high, trimmed on the left, with the tagline redrawn larger in Jura SemiBold (Debian package `fonts-jura`)
