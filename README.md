# Spunky - beta channel

Spunky is a private, local-first task and calendar app for Windows. Your data
is encrypted and stays on your machine.

This repository hosts **installer releases only**. The app is developed
privately; nothing here is source code.

> **This is a beta channel.** Releases are signed with a development
> certificate, which is why installing takes the one-time trust step below.
> Before general availability, releases will move to a purchased,
> publicly-verified publisher certificate; that switch will be announced in a
> release note here and will require a one-time reinstall (your data is
> preserved).

## Install (Windows 10 1903 or newer, x64)

**Step 1 - trust the signing certificate (one time per machine).**
Download `Spunky-development-signing.cer` from the
[latest release](../../releases/latest), then run PowerShell **as
administrator** in your Downloads folder:

```powershell
certutil -addstore TrustedPeople Spunky-development-signing.cer
```

**Step 2 - install the app.**
Download `Spunky.appinstaller` from the
[latest release](../../releases/latest) and open it. Windows shows the app
and its version; click **Install**.

Install the `.appinstaller` file rather than the `.msix` - that is what turns
on automatic update checks.

## Updates

When a new version is released here, Spunky offers it the next time you
launch the app: a Windows prompt shows the new version and you choose whether
to install it. Declining never blocks the app you already have. No update is
ever applied silently.

## Uninstalling

Uninstall from Windows Settings like any app. Your data (tasks, calendar,
backups, encryption keys) is deliberately **not** deleted by an uninstall; it
lives in your user profile, not inside the app package. Reinstalling later
finds it again.
