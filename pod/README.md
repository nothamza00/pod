# Pod – retro click-wheel music player (free, iPhone + Android + desktop)

An installable web app (PWA). No App Store, no Apple developer fee, no Mac needed.

## 1. Host it (free, 3 minutes)

Apps like this must be served over HTTPS to install on an iPhone. Pick one:

**GitHub Pages**
1. Create a free GitHub account → New repository → name it `pod`, set Public.
2. Upload all 5 files from this folder (index.html, manifest.json, sw.js, icon-192.png, icon-512.png).
3. Settings → Pages → Source: `main` branch, `/ (root)` → Save.
4. After ~1 minute your app is at `https://YOURNAME.github.io/pod/`

(Netlify Drop at app.netlify.com/drop also works: drag the folder in, done.)

## 2. Install on iPhone

1. Open your link in **Safari** (must be Safari).
2. Tap Share → **Add to Home Screen** → Add.
3. Open "Pod" from the home screen. It now runs full screen and works offline.

## 3. Controls

| Action | How |
|---|---|
| Scroll list | Slide finger around the wheel |
| Select / play-pause | Tap the centre button |
| Back | Tap MENU |
| Next / previous | Tap ⏭ / ⏮ |
| Play / pause | Tap ▶︎❙❙ |
| Seek (Now Playing) | Slide around the wheel |

Clicks are synthesized sound (Settings → Click Sound). iPhone must not be on silent mode.

## 4. Add your own songs (offline)

Music → Import Songs… → pick audio from Files (iPhone storage, iCloud, or SD card via a card reader/USB-C).
Files are copied into the app's private storage, so they play with no internet.
- Name files `Artist - Title.mp3` for correct tags.
- Add a `.lrc` file with the same name (select both) for synced lyrics offline.

## 5. Link Spotify (one-time, free)

Spotify requires every app to have its own Client ID; this cannot be skipped. It is free and takes 2 minutes:

1. Go to developer.spotify.com/dashboard → create app.
2. Redirect URI: your exact app URL, e.g. `https://YOURNAME.github.io/pod/` (with trailing slash is the page location; it must match exactly what the app uses).
3. Tick "Web API". Save, copy the **Client ID**.
4. In Pod: Spotify → Client ID → paste → Link Spotify → approve once.

After that it stays linked (no login again). Pod shows what Spotify is playing, with real-time synced subtitles, and the wheel controls Spotify play/pause/next/prev (control needs Spotify Premium).

## 6. Ambient mode

Main menu → Ambient. Dark animated screen with clock, song and live lyric line; keeps the screen awake. Tap to exit.

## Honest limits (iOS rules, not bugs)

- **Background**: local songs keep playing with the screen locked and show lock-screen controls. Lyrics tracking pauses when iOS suspends the page; Spotify audio itself plays in the Spotify app, so it is unaffected.
- **Spotify audio**: Pod doesn't stream Spotify audio itself (not allowed for web apps); it remote-controls and displays the Spotify app.
- **Lyrics** come from the free lrclib.net database (needs internet once per song, then cached). Some songs have none.
- **SD card**: iPhones have no slot; use a card reader and Files app import.
- iOS may clear storage of web apps unused for weeks; keep a copy of your music elsewhere.
