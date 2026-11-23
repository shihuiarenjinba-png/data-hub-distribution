# Public sample release policy

The repository tree contains policy, schemas, and validation code only. Data files are attached to a tagged GitHub Release so replacing a sample does not leave prior sample files in commit history.

The publisher must:

1. Derive a per-series observation window from the actual latest observation and configured public lookback.
2. Validate that every retained observation is inside the window and that e-Stat remains candidate-only.
3. Build the manifest from the exact bytes that will be uploaded.
4. Create a new release using the `sample-YYYYMMDDTHHMMSSZ` tag.
5. Download each public asset using an unauthenticated HTTPS request and verify JSON/CSV shape, row counts, byte size, and SHA-256.
6. Delete older `sample-*` releases only after every new asset has passed public GET and digest checks.

Full-history data and member data belong only in the private data-Hub repository. This repository's releases do not enforce member access and must never contain those datasets. Previous downloaded copies cannot be recalled.

A repository-scoped fine-grained token is used only by the private data-Hub publisher workflow. It should have Contents read/write access only to this repository. The secret value must never be logged, committed, or exposed to a client.
