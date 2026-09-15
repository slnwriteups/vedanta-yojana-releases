# Vedanta Yojana — Android Releases

Official public Android APK releases for the Vedanta Yojana mobile app.

This repository is a **binary release host only** — it contains no application source code, no build tooling, and no development history. It exists so that signed release APKs remain publicly downloadable independent of the private source repository.

Each release lists:

- The signed `app-release.apk` binary
- A `.sha256` checksum file for verifying the download

Verify a download with:

```
shasum -a 256 -c app-release.apk.sha256
```
