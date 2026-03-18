# Note Bible

A minimal Bible reader and note-taking app. Read, highlight, annotate — nothing else.

## What it does

- Read the Bible in KRV (개역한글) and KJV side by side
- Write notes attached to specific verses
- Search your notes
- Works offline
- Installs as an app on your phone or desktop (PWA)

## What it doesn't

- No account or login
- No server or cloud sync
- No social features
- No ads, no tracking

## Install

**Mobile (iOS / Android)**

1. Open the app URL in Safari (iOS) or Chrome (Android)
2. Tap the share icon → "Add to Home Screen"
3. Tap Add — it installs like a native app

**Desktop (Chrome / Edge)**

1. Open the app URL
2. Click the install icon in the address bar (or browser menu → "Install")
3. It opens as a standalone window from your taskbar or dock

## Development

Requires a local server — the app fetches Bible data files, which browsers block over `file://`.

```bash
git clone https://github.com/kenehong/note-bible.git
cd note-bible
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

No build step, no dependencies to install.

## Data

All notes are stored in your browser's IndexedDB (`BibleNoteDB`). Nothing leaves your device.

There is no built-in export or backup — clearing browser data or uninstalling the app will erase your notes. Use your browser's developer tools to export IndexedDB data if needed.

## License

MIT
