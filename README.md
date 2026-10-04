<p align="center">
  <img src="docs/hero.png" alt="Rennblock: the telemetry overlay, with a Ferrari 296 GT3 in Assetto Corsa EVO" width="100%">
</p>

<p align="center">
  <a href="https://github.com/benghe-raul/rennblock-status/releases/latest/download/Rennblock.exe"><img src="docs/download.png" alt="Download for Windows" height="60"></a>
</p>

<p align="center">
  <b>Live telemetry overlays for Assetto Corsa EVO.</b><br>
  Know whether this lap is faster while you are still driving it, see every brake and throttle input,<br>
  and keep every lap you have ever driven, on your own PC.
</p>

<p align="center">
  Windows 10 or 11, 64-bit &nbsp;·&nbsp;
  <a href="https://github.com/benghe-raul/rennblock-status/releases/latest">What's new</a> &nbsp;·&nbsp;
  <a href="INSTALL.md">Install guide</a> &nbsp;·&nbsp;
  <a href="INSTALL.md#if-windows-blocks-rennblock">If Windows blocks it</a>
</p>

<br>

<p align="center">
  <img src="docs/overlay.gif" alt="The telemetry overlay moving: delta, lap times, the throttle and brake trace, the pedals, gear and speed" width="100%">
  <br><sub>The telemetry overlay as Rennblock draws it, laid over a frame from the game.</sub>
</p>

## A telemetry overlay that tells you how the lap is going

- **Delta, live against your best lap.** Green while you are ahead, red when you are behind, and the ring fills as the gap grows.
- **Lap times:** current, last, predicted and best.
- **The throttle and brake trace** of the last seconds: how hard you braked, how long you coasted, when you went back to full power.
- **Pedal bars** for clutch, brake and throttle.
- **Gear, speed and fuel**, with the rev arc.
- **TC and ABS** turn the bars and the trace aqua and orange only when they act, so you see exactly where the car needed help.

The game is read 200 times a second, and the overlays are native windows drawn by the app itself, on top of the game.

## Build your own overlay

<img src="docs/variants.png" alt="The telemetry overlay in five shapes: every block; delta, times and gauge; trace, pedals and gauge; delta and gauge; every block with a see-through background" width="100%">

Show only the blocks you want, in any combination. Set how see-through the background is and how opaque the whole overlay is, where the rev arc turns red (and whether the whole overlay turns red with it), speed in km/h or mph, how much delta fills the ring (0.5, 1 or 2 seconds), and the size of each overlay from 30 % to 200 %.

## Your music, on screen

<img src="docs/media.png" alt="The media overlay: cover, title, artist, position and the playback controls, with a wave" width="70%">

The media overlay shows what Windows is playing: cover, title, artist and position, with the playback controls and a wave drawn from the sound.

## Every lap, kept

<img src="docs/panel-home.png" alt="The panel's home: the driving calendar, the session, the recent laps and the personal bests" width="100%">

Rennblock saves your laps as you drive.

- **Your driving:** a calendar of the days you were on track, with this week, this month, your streak and your best day.
- **This session:** track, car and laps, live.
- **Recent laps**, each one marked valid or out.
- **Personal bests**, one per track and car, from valid laps only.

## Every overlay where you want it

<img src="docs/panel-layout.png" alt="The Layout page: a map of the screen with the overlays on it, and the size of each one" width="100%">

Drag the overlays on a map of your screen, with or without the game running. They snap to the screen's edges and to each other (hold Alt to place them freely), and each one has its own size.

## Settings that stay out of the way

<img src="docs/panel-settings.png" alt="The Settings page: start with Windows, the tray, the shortcuts and the refresh rate" width="100%">

Start Rennblock with Windows if you like, and leave it in the tray: closing the window keeps the overlays on. **Ctrl + Alt + O** shows or hides them, and the refresh rate follows your monitor or is set to 60, 120, 144 or 180 Hz.

<img src="docs/panel-overlay.png" alt="The Overlay page: each overlay on or off, with the telemetry's options open" width="100%">

## Everything stays on your PC

<img src="docs/panel-general.png" alt="The General page: Rennblock runs fully on this machine, and the local data" width="100%">

There is no account. Your laps and settings are stored in `%LOCALAPPDATA%\Rennblock` and are never uploaded anywhere; delete that folder and they are gone. Rennblock fetches only the list of versions from this page when it starts, and a new version when you choose to update.

## Updates you can trust

<img src="docs/launcher-update.png" alt="The launcher offering an update: Rennblock 0.1.10 is ready, Update now" width="80%">

You download one file, `Rennblock.exe`, once. It installs Rennblock in your user folder (no administrator rights), adds it to the Start menu, checks every file against its published fingerprint each time it starts, and offers each new version: **Update now**, **Not now** or **Skip this version**.

## Install

1. **[Download `Rennblock.exe`](https://github.com/benghe-raul/rennblock-status/releases/latest/download/Rennblock.exe)** and run it.
2. Windows may stop it, because Rennblock is not code-signed: **[here is what to do](INSTALL.md#if-windows-blocks-rennblock)**.
3. Read the privacy notice and the license, tick the box, and choose **Accept and continue**. The launcher downloads Rennblock and checks it.
4. Start Assetto Corsa EVO and drive. The telemetry overlay is on from your first lap, at the bottom centre of the screen; the panel opens from the tray icon.

The **[install guide](INSTALL.md)** walks through it with pictures.

## Questions

**Why does Windows warn me about it?**
Rennblock is an independent project and is not code-signed, so Windows does not know its publisher and asks you first. The **[install guide](INSTALL.md#if-windows-blocks-rennblock)** shows what each warning means and what to do. What you run is checked by the launcher: every file must match the fingerprint published here, in a list signed with a key built into the launcher.

**Does it send my data anywhere?**
No. Everything stays on your PC. At start the launcher reads two small public files from this page, the version list and its signature, and nothing else leaves your computer.

**Which games does it work with?**
Assetto Corsa EVO.

**How do I remove it?**
From **Settings → Apps → Installed apps**, or from the Start menu. It asks whether to keep your laps and settings or delete them.

## Support

Write to benghe.web@gmail.com. If the launcher failed, attach `%LOCALAPPDATA%\Rennblock\launcher.log`.

## How the updates are checked

This repository is not the source code. It carries the signed update list that the launcher reads:

- `manifest.json` — the current release, where to download it, and the SHA-256 fingerprint of every file that is checked each time Rennblock starts.
- `manifest.sig` — the Ed25519 signature of `manifest.json`.

The launcher accepts an update list only when that signature matches the public key built into it, so a tampered list is refused even if this repository were altered. Each release contains the launcher and the application archive, with their fingerprints written in the release notes.

---

Rennblock is an independent project. It is not affiliated with, endorsed by, or connected to Kunos Simulazioni or 505 Games.
