# Vedanta Yojana — Android Releases

Official public Android APK releases for the Vedanta Yojana mobile app.

**This is the only official place to download the Android app.**
Vedanta Yojana is open source and is distributed only through GitHub —
it is not published on Google Play or any other app store.

- **Latest release:** [v1.0.3 (versionCode 16)](https://github.com/slnwriteups/vedanta-yojana-releases/releases/latest)
- **Source code:** [slnwriteups/vedanta-yojana-source](https://github.com/slnwriteups/vedanta-yojana-source) (MIT License for the software; see its `CONTENT-LICENSE.md` for the books and written content)
- **Website:** [vedantayojana.org](https://vedantayojana.org)

This repository is a **binary release host only** — it contains no
application source code, no build tooling, and no development history.
Every APK here is built by EAS (Expo Application Services) and signed
with the project's production key.

## What each release contains

- `vedanta-yojana.apk` — the signed Android app
- `vedanta-yojana.apk.sha256` — its SHA-256 checksum

## Verify a download

With both files in the same folder:

```
shasum -a 256 -c vedanta-yojana.apk.sha256
```

Then confirm the signing certificate (Android SDK build-tools):

```
apksigner verify --print-certs vedanta-yojana.apk
```

The certificate SHA-256 must be:

```
6f1a6565d8c6c3ab3e2fd76990ca1374d56d2fa3530e50613869fe34cbab8597
```

Full guide: [APK Verification Guide](https://github.com/slnwriteups/vedanta-yojana-source/blob/main/docs/APK-VERIFICATION.md).

## Updates

From v16 (1.0.3) on, content and app fixes arrive automatically as
over-the-air updates — no reinstall needed. A new APK is published here
only when a change can't be delivered that way.

Upgrading an older install:

| Installed version | What to do |
|---|---|
| v13 (1.0.0) | Install v16 over it; your data is kept. The app also shows an update notice. |
| v10 (1.0.0) | No update notice appears. Download and install v16 from this page; it installs over v10 and keeps your data. |
| v14 (1.0.1) or v15 (1.0.2) | These were debug-signed test builds published on the source repository, not here. Android will not install v16 over them: uninstall first (this removes local app data), then install v16. |
