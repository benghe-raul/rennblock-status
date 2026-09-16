# Rennblock

**[Download Rennblock](https://github.com/benghe-raul/rennblock-status/releases/latest/download/Rennblock.exe)** — Windows 10 or 11, 64-bit.

Rennblock is a telemetry client for Assetto Corsa EVO. It reads the data the game
publishes while you drive, draws overlays on top of it, records your laps and shows
them in a panel that runs entirely on your own computer. There are no accounts, and
your laps are never uploaded anywhere.

Run the file you downloaded. Windows will warn about an unknown publisher, because the
program is not code-signed yet: choose **More info → Run anyway**. The launcher then
installs Rennblock, verifies it and keeps it up to date.

## What this repository is

This is not the source code. It carries the signed update list that the launcher reads:

- `manifest.json` — the current release, where to download it, and the SHA-256
  fingerprint of every file that is checked each time Rennblock starts.
- `manifest.sig` — the Ed25519 signature of `manifest.json`.

The launcher accepts an update list only when that signature matches the public key
built into it, so a tampered list is refused even if this repository were altered.
Each release below contains the launcher and the application archive, with their
fingerprints written in the release notes.

## Support

Write to benghe.web@gmail.com. If the launcher failed, attach
`%LOCALAPPDATA%\Rennblock\launcher.log`.

---

Rennblock is an independent project. It is not affiliated with, endorsed by, or
connected to Kunos Simulazioni or 505 Games.
