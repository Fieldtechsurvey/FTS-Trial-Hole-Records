# FTS Trial Hole Records — PWA prototype V0.1

Standalone offline-capable field recorder for Android and iPhone, hosted using GitHub Pages. **This is a testing prototype, not yet approved for production field investigations.**

## Publish on GitHub Pages

1. Open your new `Fieldtechsurvey/FTS-Trial-Hole-Records` repository.
2. Choose **Add file → Upload files** and upload all seven files in this folder: `index.html`, `app.js`, `style.css`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`. You can also upload this `README.md`.
3. Commit the uploaded files to `main`.
4. Open **Settings → Pages → Build and deployment**; select **Deploy from a branch**, branch `main`, folder `/ (root)`; save.
5. Open `https://fieldtechsurvey.github.io/FTS-Trial-Hole-Records/` in a phone browser while online. On iPhone choose Safari Share → Add to Home Screen; on Android choose Chrome Install app or Add to Home screen.
6. Open once while connected and then TEST in airplane mode. Create a sample project, record TH1, photograph and export a complete JSON backup. Reopen the app and verify the data persists.

## Included

- FTS-branded project creation and recall
- Trial hole name, method, surface cover (including Agricultural field), target and actual depths, optional BNG coordinates
- Multiple sequential ground layers, wet indicator, notes, and refusal cause
- Multiple compressed Before and After photos
- Project-specific JSON backup/restore including photos, and CSV export (one row per layer)
- Local IndexedDB data storage and service worker offline shell

## Important limits

- **No map or GPS in V0.1.** Planned coordinates are manual fields, ready for import and mapping in a later stage.
- Data is saved when **Save trial hole to phone** is pressed. Draft form edits do **not** autosave yet.
- Browser storage can be cleared or evicted, and losing a phone loses unsynchronised records. Download full JSON backups regularly and copy them to separate storage. JSON backups may be large with many photographs.
- No cloud sync, account login, encryption, shapefile/CSV location importer, CAD viewer, PDF or DXF export in this prototype.
- Public GitHub Pages exposes application code but does not automatically upload field records. **Do not upload actual project JSON/CSV backups, confidential client data or site photographs to the repository.**
- Photo capture and installed-PWA behaviour must be tested on each target phone. This app is not a substitute for an independently verified field-data retention plan.
- The OHL app and its existing IndexedDB storage are untouched: this app has a separate database and cache namespace.
