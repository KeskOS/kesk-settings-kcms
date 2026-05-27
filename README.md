# kesk-settings-kcms

`kesk-settings-kcms` is a compatibility shim package that exists only to pull in the renamed `keskos-settings` package.

## What this is

This repository preserves the older package name used by earlier KeskOS setups so upgrades can move users onto `keskos-settings` without manual intervention.

## Role in KeskOS

Compatibility package.

## Package name

```txt
Package: kesk-settings-kcms
Repo: [keskos]
Architecture: any
```

## What it installs or provides

- Installs no runtime files of its own.
- Depends on `keskos-settings` so the current settings package is installed automatically.

## Commands and launchers

- This package does not install commands or GUI launchers; use `keskos-settings` after installation.

## Config, logs, and state

- This package does not create config files, logs, or systemd units.

## Dependencies

- Runtime dependency: `keskos-settings`.
- Build with `makepkg -s --noconfirm`.

## Build

```bash
makepkg -s --noconfirm
```

## Packaging notes

- Keep this repo lightweight until old package references disappear from the user base.
- The real functionality lives in `keskos-settings`.

## Troubleshooting

- If the old package name is still being referenced, installing this shim should resolve it automatically.

## Docs website export notes

- Docs site usage is mainly a migration note and rename notice.
