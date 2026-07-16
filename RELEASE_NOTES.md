# Release Notes

## v1.0.4
GH#845 — republish with American English (en-US) content, completing the source-only GH#805 flip that never reached the Hub. Copy only — no functional or behaviour change.

## v1.0.3
GH#657 Framing B — republish wave. Bundle now ships `dependencies: []` in its signed manifest (injected by `publish-skrpt.mjs` for `--shared` publishes), so the App's dep-referenced install pipeline (post-PR #47) accepts it on standalone update via Hub Update-all. No content changes.

## v1.0.2
Fix-forward after v1.0.1 publish failure. v1.0.1 release artefact published to GitHub, but the per-skrpt CI's "Register version with Hub API" step failed at the SKRPT_ID lookup — `/api/skrpts/<slug>` had just been filtered to `entry_type='skrpt'` by Row 4a (`d8dfdf3f`), and CF Pages deployed mid-batch (between this dep's queue position and the previous one's), so shared-objects 404'd. v1.0.1's release artefact is therefore orphaned (no D1 versions row). v1.0.2 republishes after caller-release.yml is updated to extract SKRPT_ID from the signed manifest's top-level `id:` field locally (K-037 canonical), so the lookup no longer depends on the filtered endpoint. Per Adj-1 freeze-window discipline: fix-forward, no re-tag of v1.0.1.

## v1.0.1
GH#638 Row 13 — republish with `manifest.id` aligned to Hub catalog UUID. Pre-K-037 v1.0.0 bundles carried a local `manifest.id` that differed from the catalog's UUID for this slug, causing engine STEP 4d strict-UUID match to halt consumer installs (`ComposedStagingError`). Row 5 (`0d9c9dbe`) reconciled the source file but did not republish the signed bundle; v1.0.1 ships the corrected `manifest.id` end-to-end. No content changes.

## v1.0.0
Initial catalog release as independent shared object (GH#612 Wave 3).
