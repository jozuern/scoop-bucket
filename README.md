# Scoop bucket for Tunero

[![Tests](https://github.com/jozuern/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/jozuern/scoop-bucket/actions/workflows/ci.yml) [![Tunero update](https://github.com/jozuern/scoop-bucket/actions/workflows/tunero-update.yml/badge.svg)](https://github.com/jozuern/scoop-bucket/actions/workflows/tunero-update.yml)

[Scoop](https://scoop.sh) manifest for [Tunero](https://github.com/jozuern/Tunero), a PC optimizer for Windows 11.

## Install

```pwsh
scoop bucket add tunero https://github.com/jozuern/scoop-bucket
scoop install tunero/tunero
```

Tunero then appears in the Start menu under Scoop Apps. It asks for administrator rights on every start, because it changes system settings.

## Updates

```pwsh
scoop update tunero
```

"Update now" in the app runs this command for you. The workflow "Tunero update" of this bucket checks for a new Tunero release every few hours. It updates the manifest only when the release's exe matches its SHA-256 file and carries Tunero's update signature, checked with the public keys in `keys/` (Tunero's release key and its offline backup key).

## Uninstall

Settings > Uninstall in the app undoes its changes if you want, runs `scoop uninstall tunero` and removes its data folder (`%ProgramData%\Tunero`, with the backups of your changes). `scoop uninstall tunero` on its own keeps that folder.

## Problems

Problems with the app: [Tunero issues](https://github.com/jozuern/Tunero/issues). Problems with the manifest (wrong hash, failed install): an issue in this repository.
