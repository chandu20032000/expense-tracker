# Expense Tracker — Local Chrome App

A standalone expense and monthly cash-flow tracker designed to run on your own device. This package is configured as an installable Progressive Web App (PWA).

## Local-only privacy

- This package is intended to be run locally, not published to a public GitHub Pages website.
- App data is stored in browser storage on the device.
- The app source has no external API calls, analytics, remote fonts, or third-party JavaScript dependencies.
- The service worker caches the app shell so it can reopen offline after the first successful local load.
- No cloud sync is provided. Clearing browser data or changing devices can lose access to stored records; export/back up data regularly.

**Important:** Chrome does not allow service workers or PWA installation from a `file://` URL. To install it, serve this folder from `localhost` on the same device. The local server does not need internet access.

## Install on desktop Chrome

1. Extract this ZIP to a folder on your computer.
2. Install Python 3 if it is not already installed.
3. Open a terminal/Command Prompt in the extracted folder.
4. Run:

   ```bash
   python -m http.server 8765 --bind 127.0.0.1
   ```

5. In Chrome on that same computer, open `http://localhost:8765`.
6. Wait for the page to load, then use Chrome's **Install** icon in the address bar or **Menu → Save and share → Install page as app** (wording varies).
7. Keep the folder and local server available when first installing. After the app shell has been cached, it can reopen offline.

To stop the local server, return to the terminal and press `Ctrl+C`.

## Android Chrome

A local-only install on Android requires the web server to run on the Android device itself (or a local development environment that binds to the device's loopback interface). A server running on your PC at `localhost` is not the same as `localhost` on your phone. For an easy Android-only local setup, use a trusted Android local web-server app, serve this folder on `127.0.0.1`, open its local URL in Chrome, and choose **Add to Home screen / Install app** if Chrome offers it. Do not expose the server to your Wi-Fi network if you want it restricted to the device.

## Files

- `index.html` — application
- `manifest.webmanifest` — install metadata
- `sw.js` — offline app-shell cache
- `icon-192.png`, `icon-512.png` — install icons
- `LICENSE` — MIT License
- `TERMS.md` — Terms and Conditions

## License

See [LICENSE](LICENSE).

## Terms

See [TERMS.md](TERMS.md).
