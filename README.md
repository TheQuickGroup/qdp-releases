# QDP releases

Public release feed for **QDP — Quick Data Products**. The application source lives in a private
repository; this repo holds only the built installers and the Tauri auto-update manifest.

## Assets per release
- **macOS:** `QDP_<version>_aarch64.dmg` (fresh install) + `QDP.app.tar.gz` / `QDP.app.tar.gz.sig` (the in-app updater payload)
- **Windows:** `QDP_<version>_x64-setup.exe`, `QDP_<version>_arm64-setup.exe` (+ `.sig`)
- **`latest.json`** — the update manifest the installed app polls

## How it works
Each GitHub Release here is published automatically by the `release` workflow in the private source
repo when a `v*` tag is pushed there. The installed app checks
`https://github.com/Alexveeuk/qdp-releases/releases/latest/download/latest.json` on launch and prompts
to update whenever a newer **signature-verified** version is available.

## Licence, terms and privacy
QDP is proprietary software. Copyright © 2026 Alexander Viljoen. All rights reserved.

Use of QDP is governed by the [QDP Terms of Use](TERMS.md), which the app asks you to accept when
you create an account or sign in. QDP is licensed, not sold; see [LICENSE](LICENSE).

The [QDP Privacy Notice](PRIVACY.md) explains what personal information QDP collects about its
users, why, how long it is kept, and your rights.
