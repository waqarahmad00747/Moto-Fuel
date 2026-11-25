# MotoFuel on Android (v1.4.1)

MotoFuel keeps your data **inside the browser on your phone**. Nothing is sent anywhere. Because Android browsers can clear site data, always keep a backup.

## Recommended: install it as an app (most reliable)
Android only lets a page store data safely and work offline when it is opened from a **web address** (https, or `http://localhost`), not from a loose file.

1. Put the folder **MotoFuel-Android** (index.html, manifest.webmanifest, sw.js and the three icon PNGs) on any static web host you trust (for example GitHub Pages, Netlify, Cloudflare Pages, or your own server). All files must stay together in the same folder.
2. Open that address once in **Chrome** on your phone.
3. Chrome menu (⋮) → **Add to Home screen / Install app**.
4. After the first load the app opens from your home screen and **works fully offline**. Your records stay on the phone only; the host never sees them.

## GitHub Pages step by step (so it installs as a real app, not a "PC page")
1. Create a **public** repository and upload **every file from the `MotoFuel-Android` folder directly into the repo root** (index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png, icon-maskable-512.png). Do not rename index.html and do not put the files in a sub-folder.
2. Repository **Settings → Pages → Deploy from a branch → main / (root)**. Wait 1–2 minutes.
3. On the phone open **https://YOURNAME.github.io/REPO/** in **Chrome** (not the github.com page, which only shows source code).
4. If it looks like a PC page: Chrome menu ⋮ → turn **Desktop site OFF**, reload. MotoFuel also shows a warning in Settings → "Phone & install" when it detects this.
5. Install: use the **Install MotoFuel as an app** button in Settings → "Phone & install", or Chrome menu ⋮ → **Install app**. If the menu only says *Add to Home screen*, one of the files above is missing or not in the repo root: the result is just a website shortcut with the browser bar.
6. Open it from the home-screen icon: it should have no address bar.
Updating later: replace the files in the repo, open the app twice (the first load fetches the new version, the second uses it).

## Quick option: open the single file
You can also open `MotoFuel.html` directly (Files app → Chrome). It works, but:
- Some Android file viewers block browser storage. If Settings → Storage shows **"Memory only – NOT saved"**, nothing is kept; install it as above instead.
- Even when storage works, the browser may clear it. Back up after every session.

## Saving and backups (Settings → Backup)
- **Share / save backup…** (appears on Android): opens the phone's share sheet. Pick **Drive**, **Files**, e-mail or WhatsApp. This is the safest way. The backup date is recorded only when sharing actually completes.
- **Export JSON backup**: downloads the file to **Files → Downloads**.
- **Copy backup text**: copies everything as text. Paste it into Notes or an e-mail to yourself.
- **Restore**: *Choose backup file…*, or open *Can't pick a file? Restore by pasting backup text* and paste.
- Unsaved entries on **Add New Refill / Add New Oil Change** are kept automatically if Android closes the browser in the background, and come back when you reopen the app (for 7 days).

## Speed
Tab switching was made lighter for phones (cached number formatting, shorter animations, no heavy blur effects on phones, no smooth-scroll delay). In a mid-range phone simulation every tab appears in about 0.2 s or less, with 300 refills stored.

## Not tested
Only a Chromium phone emulation was tested (including install and offline from a local web server). Real Android devices, Samsung Internet, Firefox for Android, and Android WebView wrappers were not tested.
