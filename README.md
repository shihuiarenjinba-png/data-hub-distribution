# data-Hub public sample distribution

This public repository hosts only short-window, unauthenticated sample releases built from official statistics sources.

## Public data limits

- Each sample is limited to at most three calendar months per series, anchored to that series' actual latest available observation.
- Full-history and member datasets are never published here.
- Sample data is distributed as GitHub Release assets, not committed files. This avoids retaining replaced sample files in the Git tree.
- After a new release passes external download, schema, row-count, and SHA-256 checks, the publisher removes prior `sample-*` releases.
- Previously downloaded copies cannot be recalled.
- Japan e-Stat discovery results are candidate data and are not approved research series.

## Find the current sample

Open [Releases](https://github.com/shihuiarenjinba-png/data-hub-distribution/releases). Each verified sample Release contains:

- `official-bundle.json`
- `us-official-series.csv`
- `jp-estat-candidates.csv`
- `manifest.json`

Use the manifest's exact asset URLs, byte sizes, SHA-256 hashes, interval, and data status. Verify each downloaded asset before parsing it. The manifest is specific to its immutable release tag.

## Access control

This public repository has no member data and does not grant app entitlements. Authenticated or plan-limited datasets must be served by a separate server that verifies identity and contract state before reading private data. Never put private repository tokens or private release URLs in a client application.

## License and source attribution

Source publishers' terms govern their datasets. Check each source's terms before redistribution or commercial use. The manifest and each file preserve the data source and available series metadata. This repository does not imply endorsement by BLS, the U.S. Census Bureau, or Japan's e-Stat.
