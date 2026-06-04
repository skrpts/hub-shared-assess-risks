# Release Notes

## v1.0.1
GH#638 Row 13 — republish with `manifest.id` aligned to Hub catalogue UUID. Pre-K-037 v1.0.0 bundles carried a local `manifest.id` that differed from the catalogue's UUID for this slug, causing engine STEP 4d strict-UUID match to halt consumer installs (`ComposedStagingError`). Row 5 (`0d9c9dbe`) reconciled the source file but did not republish the signed bundle; v1.0.1 ships the corrected `manifest.id` end-to-end. No content changes.

## v1.0.0
Initial catalogue release as independent shared object (GH#612 Wave 3).
