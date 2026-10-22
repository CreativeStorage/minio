# Creative Storage MinIO baseline

This fork is being evaluated for Inventory product images and swatches. It is an S3-compatible object store; product identities, full-sheet counts, location balances and stock events belong to the Inventory application database.

## Approved starting point

The user explicitly requested a release **before April 2025**, rather than the current upstream branch.

- Upstream: https://github.com/minio/minio
- Release: `RELEASE.2025-03-12T18-04-18Z`
- Annotated tag object: `9969f094128406d9e9a6c1d4407f28e020b16920`
- Source commit: `dbf31af6cb0d5ea33b277b6e461cfea98262778e`
- Fork working/default branch: `css-stable`

GitHub forks retain upstream history. An inherited upstream branch is not the deployment target. Never bulk-merge current upstream into `css-stable` or build production from an unpinned `latest` tag.

## Maintenance contract

Preserve the pre-April administration Console and review later security fixes individually. An old feature baseline is not a claim that its dependencies are currently safe. Inventory known later advisories, including the April 3, 2025 security release, and backport required fixes with tests before production exposure. Keep the upstream license, notices and provenance.

A reproducible image must build from reviewed source, pin its toolchain/runtime images, and include an SBOM and vulnerability report. Test the full Console, denied anonymous access, limited application credentials, S3 object operations, persistence and backup/restore.

Deploy only through an explicit Compose environment with persistent data and non-root execution. Keep the administrator console private. Follow the confirmed host ownership: CSS-Pi retains authoritative application data; OptiPlex handles frontend/static serving and builds. Media placement and backup require an explicit design; never silently write the production NAS.

## Current state

Repository/baseline preparation only. No MinIO container, public endpoint, credentials or production media migration has been deployed by this change.

Tracking: https://github.com/CreativeStorage/minio/issues/1
Inventory: https://github.com/CreativeStorage/creative-storage-dot-dev/issues/24
