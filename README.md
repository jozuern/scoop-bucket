# Scoop bucket for Tunero

[![Tests](https://github.com/jozuern/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/jozuern/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/jozuern/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/jozuern/scoop-bucket/actions/workflows/excavator.yml)

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

"Update now" in the app runs this command for you. The Excavator workflow of this bucket checks for a new Tunero release every few hours and updates the manifest with the version and the SHA-256 from the release.

## Uninstall

Settings > Uninstall in the app undoes its changes if you want, runs `scoop uninstall tunero` and removes its data folder (`%ProgramData%\Tunero`, with the backups of your changes). `scoop uninstall tunero` on its own keeps that folder.

## Problems

Problems with the app: [Tunero issues](https://github.com/jozuern/Tunero/issues). Problems with the manifest (wrong hash, failed install): an issue in this repository.
