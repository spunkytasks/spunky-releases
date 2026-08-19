# Spunky - beta channel

Spunky is a private, local-first task and calendar app for Windows. Your data
is encrypted and stays on your machine.

This repository hosts **installer releases only**. The app is developed
privately; nothing here is source code.

> **This is a beta channel.** Since v0.1.0.7, releases are signed via Azure
> Trusted Signing under the verified publisher **Spunky Development LLC**, so
> Windows trusts them on sight - there is no certificate to trust and no
> administrator step.

## Install (Windows 10 1903 or newer, x64)

Download `Spunky.appinstaller` from the
[latest release](../../releases/latest) and open it. Windows shows the app,
its version, and the verified publisher, **Spunky Development LLC**; click
**Install**. That's it.

Install the `.appinstaller` file rather than the `.msix` - that is what turns
on automatic update checks.

> **Upgrading from 0.1.0.6 or earlier (self-signed era)?** Uninstall the old
> Spunky first, then install fresh as above - one time only, because the
> app's verified identity changed and Windows treats the signed build as a
> different app. Your tasks and settings are kept. You can also remove the
> old development certificate from Trusted People; nothing needs it anymore.


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
