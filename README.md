# UOutlook - Releases

Download page for **UOutlook**, a standalone Microsoft Outlook desktop app for Linux (an
Electron wrapper around Outlook web). This repository only hosts the signed, ready-to-install
downloads - the source lives in a separate repository.

UOutlook is an independent project and is **not affiliated with Microsoft**. "Microsoft" and
"Outlook" are trademarks of Microsoft Corporation.

## Download

Get the latest build from the [**Releases**](../../releases/latest) page:

| Platform | File |
|----------|------|
| Debian/Ubuntu (Intel/AMD) | `uoutlook_<version>_amd64.deb` |
| Debian/Ubuntu (ARM) | `uoutlook_<version>_arm64.deb` |
| Any Linux (Intel/AMD) | `UOutlook-<version>.AppImage` |
| Any Linux (ARM) | `UOutlook-<version>-arm64.AppImage` |

Each build is fully self-contained - Chromium, Node and the app are bundled, so there is nothing
else to install.

## Install

**Debian/Ubuntu:**
```bash
sudo apt install ./uoutlook_<version>_amd64.deb
```

**AppImage:**
```bash
chmod +x UOutlook-<version>.AppImage
./UOutlook-<version>.AppImage
```

The AppImage auto-updates itself from this repository. `.deb` users update via `apt`/reinstall.

## Verify your download

Each release ships `SHA256SUMS.txt` and a detached GPG signature `SHA256SUMS.txt.asc`, plus a
`.asc` next to each installer. Verify before installing:

```bash
gpg --verify SHA256SUMS.txt.asc SHA256SUMS.txt   # import the signing key first
sha256sum --check SHA256SUMS.txt --ignore-missing
```

If `gpg --verify` does not report a **Good signature**, do not install the file.

## Uninstall

- **Debian/Ubuntu:** `sudo apt remove uoutlook`
- **AppImage:** delete the file (and `~/.config/uoutlook/` to remove your session data)

---

UOutlook is freeware, provided as-is without warranty. A personal project by Raul Bento
(Bentosoft, https://bentosoft.net).
