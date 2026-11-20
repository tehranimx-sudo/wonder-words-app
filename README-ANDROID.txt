WONDER WORDS ACADEMY — ANDROID APP (FREE PWA)
================================================

WHAT THIS IS
This package turns the existing Wonder Words + Ollie offline learning website into an installable Android web app (PWA). It opens from an app icon, can run full-screen, and caches its files so the learning activities work offline after the first successful online visit.

It is NOT an APK and it is not published in Google Play. It is the simplest no-cost route for one family using one tablet. No Play Store developer fee and no paid app builder are needed.

WHAT IS INCLUDED
- index.html: your existing Wonder Words Academy with local learner profiles and Ollie.
- manifest.webmanifest: Android app name, display mode and icons.
- sw.js: service worker that caches the app shell for offline use.
- icons/: app icons in Android-friendly sizes.

FREE HOSTING USING GITHUB PAGES
A PWA must be opened from a secure HTTPS address for service-worker installation. GitHub Pages can serve a public repository over HTTPS and is available to GitHub Free users for public repositories.

1. On a computer, create or sign in to a free GitHub account at https://github.com/.
2. Create a NEW repository. Call it wonder-words-app. Set visibility to PUBLIC.
3. Extract this ZIP file.
4. In the new GitHub repository, choose Add file → Upload files.
5. Upload the contents of this folder (index.html, manifest.webmanifest, sw.js, and the icons folder). Do not upload the ZIP itself. Keep the folder structure exactly as shown.
6. Commit the files.
7. Open repository Settings → Pages.
8. Under Build and deployment, choose Deploy from a branch; select main and /(root); save.
9. GitHub will show the website address, usually https://YOUR-USERNAME.github.io/wonder-words-app/.
10. Open that HTTPS address in Chrome on the Android tablet while the tablet is online. Wait for the app to finish loading; reload once so the offline cache is prepared.

INSTALL ON THE ANDROID TABLET
1. Open the published address in Google Chrome on Android.
2. Tap the three-dot menu (⋮) at the top right.
3. Tap Install app (sometimes shown as Install and create shortcut or Add to Home screen).
4. Confirm Install. The Wonder Words icon will appear on the tablet's home screen/app launcher.
5. Open Wonder Words from that icon. After the first successful load, turn on Airplane mode and test that lessons and Ollie still open.

If Chrome shows an Install app button inside Wonder Words, you can use that too. Menu wording varies slightly by Android/Chrome version. Chrome's official instructions are at https://support.google.com/chrome/answer/9658361.

KEEPING YOUR FAMILY PROGRESS
- Create a profile for your child and one for the parent if you want separate progress.
- Open Family Control Panel for the family scoreboard, settings and local backup.
- Profiles, stars, scores, shop purchases and Ollie conversations are stored in the browser/app storage on THIS tablet. They are not uploaded to GitHub and are not synchronized to another phone or tablet.
- Because this is a new HTTPS app address, it has separate browser storage from an older file:// copy. Before switching, open the OLD version, use Family Control Panel → Export family backup, then open the NEW installed PWA → Family Control Panel → Import family backup. Keep the JSON backup file safe.
- Do not clear Chrome/site data or uninstall the app unless you have exported a backup first.
- Keep opening the app from the same published URL so its saved progress stays with the same app origin.

PRIVACY AND PUBLIC HOSTING
The GitHub Pages site itself is publicly reachable and the app's HTML/JavaScript files are public. Do not put a child's private information in the code or repository. The app's learner profiles and progress are stored locally in the tablet browser; this package adds no cloud database or analytics service. The public site does not include any family profile data unless you deliberately upload a backup file (do not do that).

OFFLINE NOTES
- The first visit and installation need internet so Chrome can download the app and its cache.
- After the shell has cached successfully, the built-in learning games and Ollie work offline.
- Speech uses Android's installed text-to-speech voice. Voice availability may vary; download an English voice in Android text-to-speech settings if needed.
- Hosting is free under the documented GitHub Pages public-repository plan, but GitHub account terms and product limits can change.

UPDATES
To publish a newer app version, replace the files in the same repository and commit them. The service worker uses a versioned cache. If you substantially change offline assets, bump CACHE_VERSION in sw.js before publishing. Keep the app at the same URL to retain its on-device data.

TROUBLESHOOTING
- No Install app option: make sure the site URL begins with https://, open it in Chrome, and reload after the page has fully loaded.
- App not opening offline: visit it once while online, wait for it to finish loading, then refresh once before testing Airplane mode.
- Progress missing: check that you opened the exact same published URL and browser profile; restore a family JSON backup if you have one.
- Need help: the easiest next step is to share the GitHub Pages URL (not any backup JSON) so setup can be checked.
