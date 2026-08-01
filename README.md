# DataLounge preservation archive

This repository contains a complete public-content preservation snapshot of
DataLounge captured before the site became unavailable.

## Contents

This repository contains the archive manifest and verification checksums. The
GitHub release contains every archived byte, in split 7z volumes:

- `datalounge-raw.7z.*`: exact compressed post-feed batches
- `datalounge-site.7z.*`: exact captured HTML pages and hosted assets
- `datalounge-databases.7z.*`: preservation manifests and searchable mirror

The database volume set includes:

- `archive.sqlite3`
- `rows.sqlite3`
- `local_mirror.sqlite3`

## Capture summary

- 30,343,367 post records
- 856,417 indexed threads
- 852,217 successfully saved pages/assets
- 4,819,248,552 bytes of compressed raw post batches
- 8,386,895,412 bytes of successfully saved page/asset content
- 20,904 expected HTTP 404 responses for deleted or unavailable pages

The archive is release-only to avoid putting multi-gigabyte generated data in
normal Git history.

## Verification

Verify any downloaded release volumes against `SHA256SUMS.txt`. On Windows
with 7-Zip installed, download every part of a set into the same folder and
extract with:

```powershell
7z x datalounge-site.7z.001
7z x datalounge-raw.7z.001
7z x datalounge-databases.7z.001
```

On Linux or macOS, install `7zz` and use the same commands.
