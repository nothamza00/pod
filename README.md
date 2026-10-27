# Pod: retro click-wheel music player (free, iPhone / Android / desktop)

Installable web app (PWA). No App Store, no developer fee, no Mac.

## Files (put ALL of these in the root of your GitHub repo)
index.html, config.js, sw.js, manifest.json, icon-192.png, icon-512.png

## Update an existing install
GitHub repo → Add file → Upload files → drop the new files (same names replace the old ones) → Commit.
The app now always loads the newest version when online. Close and reopen it once or twice to pick up an update.

## Install on iPhone
Open your link in **Safari** → Share → Add to Home Screen → keep **Open as Web App ON** → Add.
Open Pod from the home-screen icon (full screen, works offline).

## Controls
| Action | How |
|---|---|
| Scroll / seek | Slide your finger around the wheel (it rotates and ticks) |
| Select / play-pause | Tap the centre |
| Back | Tap MENU |
| Next / previous / play-pause | Tap the icons on the wheel |
Laptop: mouse wheel over the wheel, arrow keys, Enter, Esc, Space.

## Music and playlists
- Music → Import Songs → pick files (name them `Artist - Title.mp3`). Add a same-named `.lrc` for offline synced lyrics.
- Playlists → New Playlist… → name it. Inside a playlist: Play, Shuffle, Add From Library…, Import Files Here…, Rename, Delete.
- Main menu has Shuffle and Repeat (Off / All / One).

## Spotify (one-time setup by YOU, the app owner)
Spotify requires every app to have a Client ID. You create it once, then users never type anything.
1. developer.spotify.com/dashboard → Create app. Tick **Web API**.
2. Redirect URI: your exact app link, e.g. `https://nothamza00.github.io/pod/`
   (in Pod: Settings → Spotify Setup → Copy Redirect URI shows it exactly).
3. Copy the **Client ID**.
4. On GitHub open `config.js` → pencil icon → paste it between the quotes → Commit.
5. Anyone now taps **Spotify → Link Spotify**, approves once, done.

**Spotify's limits (their rules since Feb 2026, not Pod's):**
- The app owner needs Spotify **Premium** for the app to work.
- A new Development-mode app allows only **5 users**, and you must add each person's Spotify email under User Management in the dashboard (they get an error otherwise).
- More users requires Spotify's "Extended Quota" approval, which is intended for businesses.
- Controlling playback (play / pause / next) needs the listener to have Premium; showing what's playing and lyrics works for free accounts.
- Pod shows and controls the Spotify app. Spotify's own audio can't be played inside a web app, and offline Spotify downloads can't be imported.

## Ambient mode
Main menu → Ambient. Colour clouds, clock, song and live lyric line; screen stays awake. Tap to exit.

## iPhone notes
- Click sounds also play with the silent switch on (iOS 16.4+). Tap the wheel once after opening the app to wake audio.
- Haptic ticks work on newer iOS versions only (Settings → Haptics to turn off).
- Local songs keep playing with the screen locked. iOS may pause lyric updates while locked.
- iOS can clear web-app storage if the app is unused for weeks: keep a copy of your music.
