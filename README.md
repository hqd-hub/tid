# Tid

A private PWA for capturing and reflecting on moments with the people closest to you.

## Deploy (GitHub Pages)
1. Create a repo (e.g. `tid`) and upload `index.html`, `sw.js`, `manifest.json` and the three `icon-*.png` files.
2. Settings → Pages → Deploy from branch `main`, root folder.
3. Open `https://<user>.github.io/tid/` in Safari on the iPhone → Share → "Add to Home Screen".

The code contains no personal data. Names are entered on first launch and stored only on the phone.

## Google Drive backup
In the app: Settings → Backup → "Sådan får du et Client ID". The app shows the exact origin and redirect URI to register.
Scope `drive.file`: the app can only see the backup file it creates itself (`Tid-backup.tid`).
The backup is encrypted on the phone with AES-256-GCM (PBKDF2-SHA256, 310k iterations) before upload.

## Updating
Bump `CACHE` in `sw.js` when you change `index.html`.
