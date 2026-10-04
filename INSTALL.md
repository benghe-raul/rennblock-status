# Installing Rennblock

Rennblock runs on Windows 10 or 11, 64-bit, next to Assetto Corsa EVO. You need one file; the launcher in it does the rest and keeps Rennblock up to date.

## 1. Download

**[Download `Rennblock.exe`](https://github.com/benghe-raul/rennblock-status/releases/latest/download/Rennblock.exe)**

## 2. Run it

Double-click `Rennblock.exe`. If Windows stops it, see **[If Windows blocks Rennblock](#if-windows-blocks-rennblock)** below, then come back here.

## 3. Read and accept

<img src="docs/launcher-terms.png" alt="The launcher's first screen: the privacy notice and the license, with the box ticked and Accept and continue" width="80%">

The launcher shows the privacy notice and the license. Tick the box and choose **Accept and continue**.

## 4. Let it download

<img src="docs/launcher-download.png" alt="The launcher downloading Rennblock 0.1.10, at 60 %" width="80%">

The launcher downloads Rennblock and checks every file against its published fingerprint. It installs in your user folder, so no administrator rights are needed, and it adds Rennblock to the Start menu and to Installed apps.

## 5. Drive

Start Assetto Corsa EVO and go on track. The telemetry overlay is on from your first lap, at the bottom centre of the screen.

The panel opens from the Rennblock icon in the tray, next to the clock. There you can switch each overlay on or off, choose what it shows, place it on the screen and see your laps.

## Updates

<img src="docs/launcher-update.png" alt="The launcher offering an update: Rennblock 0.1.10 is ready, Skip this version, Not now, Update now" width="80%">

When a new version is out, the launcher offers it as Rennblock starts: **Update now**, **Not now** or **Skip this version**.

## Removing it

Open **Settings → Apps → Installed apps**, find Rennblock and choose **Uninstall**, or use the Start menu. It asks whether to keep your laps and settings or delete them.

## If Windows blocks Rennblock

Rennblock is an independent project and is not code-signed, so Windows does not know its publisher. Depending on how your PC is set up you may see one of these messages.

### "Windows protected your PC"

This is SmartScreen. Choose **More info**, then **Run anyway**.

### "Smart App Control blocked an app that may be unsafe"

Smart App Control lets only apps it already knows, or signed ones, run, and it checks them every time they start, so it has no Run anyway button. Rennblock can run only while it is off:

1. Open **Windows Security → App & browser control → Smart App Control settings**.
2. Choose **Off**.
3. Run `Rennblock.exe` again.

Smart App Control is on only on some PCs with a fresh installation of Windows 11.

### "The app you're trying to install isn't a Microsoft-verified app"

Your PC is set to install apps from the Microsoft Store only. Open **Settings → Apps → Advanced app settings → Choose where to get apps**, pick **Anywhere**, and run `Rennblock.exe` again.

## Something went wrong

Write to benghe.web@gmail.com and attach `%LOCALAPPDATA%\Rennblock\launcher.log`.
