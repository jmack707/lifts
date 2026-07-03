# 🏋️ Lifts — Workout Tracker

A simple, private workout tracker that runs entirely in your browser. No accounts, no servers, no tracking. All your data stays on your own device.

**[▶️ Open the app](https://YOUR-USERNAME.github.io/lifts/)** *(replace with your URL after setup)*

---

## Features

- **Programs** — follow a structured routine (StrongLifts 5×5, GZCLP, and 5/3/1 built in) that rotates through workout days and tells you exactly what to lift next
- **Prescribed sets** — the app pre-fills each set's target weight and reps from your working weight (or a percentage of your training max for 5/3/1); AMRAP sets are flagged
- **Automatic progression** — hit all your sets and the weight goes up next session; miss it a few times and it deloads. 5/3/1 runs its 4-week wave off a training max that rises each cycle — all handled for you
- **Plan your own workout** — or pick exercises freely, in the order you want them
- **Log sets** — weight and reps for each set, with add/remove set and one-tap complete
- **Warm-up sets** — one tap builds a bar → 50/70/90% ramp toward your working weight, rounded to loadable plates
- **kg or lb** — switch units anytime; plate inventory and bar weight follow
- **Bodyweight exercises** — leave weight blank; the app tracks reps (and uses your bodyweight for volume if set)
- **Rest timer** — auto-starts when you check off a set, with a countdown ring, beep, and vibration
- **Personal records** — automatic PR detection with a confetti celebration 🎉
- **History** — every past session, grouped by month
- **Progress charts** — estimated 1RM, session volume, and weekly volume over time per exercise
- **Templates** — save and reload your regular workouts
- **Plate calculator** — shows which plates to load for any target weight, from your own plate inventory
- **Streak tracking** — day streak and weekly session count
- **Backup & restore** — export/import your data as a JSON file (great with Google Drive)
- **Works offline** — installable as a phone app (PWA)

---

## Install on Your Phone

### Android (Chrome)
1. Open the app URL in Chrome
2. Tap the **⋮** menu → **Add to Home Screen**
3. It installs like a native app and works offline

### iPhone (Safari)
1. Open the app URL in Safari
2. Tap the **Share** button → **Add to Home Screen**

Your data persists automatically between sessions once installed.

---

## Your Data

All workout data is stored locally in your browser (`localStorage`). It never leaves your device.

**Back it up regularly:** open the **Exercises** tab → **Backup to Drive** to download a JSON file. Store it somewhere safe like Google Drive. To move to a new device or recover data, use **Restore from Drive** and pick that file.

---

## Hosting Your Own Copy (GitHub Pages)

1. Fork or create a repo and upload these files to the root:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`
2. Go to **Settings → Pages**
3. Under **Source**, choose **Deploy from a branch** → **main** → **/ (root)** → **Save**
4. Wait ~1 minute; your app is live at `https://YOUR-USERNAME.github.io/REPO-NAME/`
5. Update the link at the top of this README

---

## Project Structure

```
├── index.html            The entire app (HTML + CSS + JS in one file)
├── manifest.json         PWA manifest (name, icons, colors)
├── sw.js                 Service worker for offline caching
├── icon-192.png          App icon (192×192)
├── icon-512.png          App icon (512×512)
├── apple-touch-icon.png  iOS home-screen icon (180×180)
└── README.md             This file
```

## Tech

Vanilla HTML, CSS, and JavaScript — no frameworks, no build step, no dependencies. Just static files. Fonts load from Google Fonts (requires internet the first time; cached after).

## License

MIT — do whatever you like with it.
