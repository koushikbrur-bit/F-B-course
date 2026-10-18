# Course Vault – Android APK via GitHub Actions

Trusted Web Activity wrapper that opens your hosted site in Chrome (needed so Google sign-in works).

## Before you start
1. Host the site first (see the earlier course-vault-pwa package: `firebase deploy --only hosting`).
2. If your URL is not https://fb17-84855.web.app, edit the two `manifestPlaceholders` lines in `app/build.gradle`.

## Build
1. Create a new GitHub repo and upload everything in this folder
   (keep the `.github/workflows/build.yml` path exactly).
2. Open the repo's **Actions** tab. The "Build APK" workflow runs on every push
   (or click Run workflow).
3. When it finishes (~3-5 min), open the run and download the **course-vault-apk** artifact.
   Unzip it to get `app-debug.apk`, copy it to your phone and install
   (allow "install unknown apps" for your browser/file manager).

## Notes
- This is a debug-signed APK: fine for personal sideloading, not for the Play Store.
- A small URL bar shows at the top until you set up Digital Asset Links (assetlinks.json on your host).
- Needs Chrome installed on the phone.
