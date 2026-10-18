# Course Vault – website + Android APK (all in one repo)

One push does everything: publishes the site on GitHub Pages, then builds the APK that opens it.

## One-time setup (3 steps)
1. **Create a GitHub repo** and upload everything in this folder, including the hidden `.github` folder
   (GitHub Desktop or `git push` is easiest; the web uploader often skips hidden folders).
2. **Turn on Pages:** repo → Settings → Pages → Build and deployment → Source: **GitHub Actions**.
   Then go to the Actions tab and re-run the workflow (or push any change).
3. **Allow the domain in Firebase** (needed for Google sign-in):
   Firebase console → project fb17-84855 → Authentication → Settings → Authorized domains → Add domain →
   `YOURUSERNAME.github.io`  (lowercase).

## Get the APK
Actions tab → latest "Deploy site and build APK" run → Artifacts → **course-vault-apk** →
unzip → `app-debug.apk` → copy to phone and install (allow unknown sources).

## Notes
- Debug-signed APK: fine for sideloading, not for Google Play.
- Needs Chrome on the phone and internet (Firebase + fonts load online).
- A small URL bar shows at the top of the app (Digital Asset Links not configured).
- Updating the website later: edit `site/index.html`, push, done. The APK itself never needs rebuilding for content changes.
