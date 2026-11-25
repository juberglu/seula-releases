# Seula — downloads

Public downloads and checksums for **Seula**, a photo culling app for macOS.

[seula.app](https://seula.app/) · [User guide](https://seula.app/help/) ·
[Release notes](https://seula.app/releases/) ·
[Mac App Store](https://apps.apple.com/app/id6786344845)

This repository holds the released disk images. The source code is not here.

## Install

Download the latest DMG:

**[Seula.dmg](https://github.com/juberglu/seula-releases/releases/latest/download/Seula.dmg)**

Or with Homebrew:

```sh
brew install --cask juberglu/seula/seula
```

Every build is signed with a Developer ID certificate and notarized by Apple,
so it opens without a Gatekeeper warning. Requires macOS 12 or later; universal
for Apple silicon and Intel.

## What Seula is

Seula is the step before your editor: you go through the frames from a shoot
and choose the keepers. It is not a photo editor and not a library manager.

- Opens a folder straight from disk. No import, no catalog, no library to
  maintain. RAW+JPEG and RAW+HEIF pairs read as one photo.
- Groups a burst into a single stack from capture time and image content, and
  steps through the folder's stacks one at a time so the rejects can be marked
  in one undoable action.
- Suggests which photo to review first in each stack and says why, such as
  sharper focus or open eyes. The analysis runs on your Mac (macOS 15 or
  later).
- Survey, Compare and Blink Compare for frames that are too similar to
  separate at a glance; focus peaking and autofocus point overlays for
  sharpness.
- Stars, color labels and pick/reject flags are written as standard XMP, which
  Lightroom, Capture One and other XMP-aware tools read, or kept in Seula
  without touching the files.
- HDR photos are shown at full brightness on a display with the headroom for
  it, with warnings for blown highlights and blocked shadows.
- Reads RAW files from Canon, Nikon, Sony, Fujifilm, OM System and Olympus,
  Panasonic, Pentax, Leica, Hasselblad, Phase One and Sigma, alongside JPEG,
  HEIC, PNG, TIFF, DNG and practically every other image format in common use.

Nothing is uploaded. No accounts, no analytics, no telemetry, no cloud
scoring: the work happens on your Mac.

## Verifying a download

Each release includes a `Seula-<version>.sha256` file:

```sh
shasum -a 256 -c Seula-1.4.0.sha256
```

You can also check the signature and notarization of the mounted app:

```sh
spctl -a -vvv /Volumes/Seula/Seula.app
```

It should report `accepted` and `source=Notarized Developer ID`.

## Updates

Seula updates itself through Sparkle: **Seula ▸ Check for Updates**. The
Homebrew cask is marked `auto_updates`, so `brew upgrade` leaves the installed
copy alone and lets the app handle its own updates.

## Support

Questions, bug reports and licensing: [support@seula.app](mailto:support@seula.app)
· [Support page](https://seula.app/support)
