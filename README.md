<p align="center"><img src="docs/images/logo.png" width="96" alt="Opal logo"></p>
<h1 align="center">Opal</h1>
<p align="center">A Liquid Glass video and music player for macOS.</p>

A Liquid Glass video and music player for macOS. Plays everything (MKV, AV1, WebM),
with subtitles, casting, and an album-art music mode.

<p align="center"><img src="docs/images/home-empty.jpg" width="720" alt="Opal's home screen before anything has been played: a play button and the text 'Play something' over a soft purple glass background"></p>
<p align="center"><sub>Screenshots show a fresh install with empty and settings screens; no real files or accounts.</sub></p>

## Install

1. Download **Opal-x.y.z.dmg** from the [latest release](https://github.com/SamDeHerdt/Opal/releases/latest).
2. Open it and drag **Opal** onto **Applications**.
3. The first time you open it, macOS may warn that it's from an unidentified developer.
   It isn't signed with a paid Apple Developer account. Fix this once by either:
   - right-clicking Opal in Applications → **Open** → **Open**, or
   - running `xattr -dr com.apple.quarantine /Applications/Opal.app` in Terminal.

<p align="center"><img src="docs/images/settings-appearance.jpg" width="560" alt="Opal Settings, Appearance pane: accent colour choices and a glass transparency slider"></p>

## Updates

Opal checks for new versions and offers to install them. Updates are signed and verified
before they're installed. What changed in each version is in [CHANGELOG.md](CHANGELOG.md).

## Issues

Found a bug? [Open an issue](https://github.com/SamDeHerdt/Opal/issues). This repository
holds the downloads and the update feed; the source code is not public.
