# 🏋️ Lifts — Workout Tracker

A simple, private workout tracker that runs entirely in your browser. No accounts, no servers, no tracking. All your data stays on your own device.

**[▶️ Open the app](https://YOUR-USERNAME.github.io/lifts/)** *(replace with your URL after setup)*

---

## Features

- **Programs** — follow a structured routine (StrongLifts 5×5, GZCLP, 5/3/1, and a 16-week RPE-based athlete program built in) that rotates through workout days and tells you exactly what to lift next
- **Supersets, RPE targets, rep ranges & timed holds** — antagonist pairs are grouped with short rest, sets can prescribe a rep range and an RPE/reps-in-reserve target, and planks/holds are logged in seconds
- **Home dashboard** — open to your stats (streak, weekly count, total sessions), a "next workout" hero that starts your program in one tap, quick actions, and recent activity
- **Per-exercise history** — every logged session for an exercise (sets, est. 1RM, PRs, notes) alongside its progress charts; open it from the 📈 button in the Exercises tab
- **Exercise library** — browse/search 1,300+ exercises (filter by body part), each with target & secondary muscles, equipment, and step-by-step how-to; add any to your list in a tap (data from ExerciseDB — see attribution below)
- **Save from anywhere** — while a workout is in progress, a bar on every other tab lets you jump back (Resume) or log it (Save) without hunting for the button; the Home tab itself shows as "Workout" mid-session
- **Focus mode** — during a workout, one exercise (or superset pair) fills the screen with a progress header and an "up next" rail; it auto-advances as you finish. Toggle to the full list anytime (☰)
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
├── data/
│   ├── exercises.json    Exercise library metadata (name, muscles, equipment)
│   └── how-to.json       English step-by-step instructions, keyed by name
├── icon-192.png          App icon (192×192)
├── icon-512.png          App icon (512×512)
├── apple-touch-icon.png  iOS home-screen icon (180×180)
└── README.md             This file
```

The two `data/*.json` files back the **Exercise Library** (Exercises tab → *Browse exercise library*). They are lazy-loaded on first use and cached by the service worker, so the library works offline afterward.

## Exercise data & attribution

The exercise library (names, target/secondary muscles, equipment, and how-to
instructions) is derived from **[ExerciseDB](https://exercisedb.dev/)** v1,
sourced via the community project
**[hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset)**.
No exercise images or animations are included. This app bundles only factual
metadata plus English instructions; if you fork or redistribute, review
ExerciseDB's terms of use for the underlying content.

## Tech

Vanilla HTML, CSS, and JavaScript — no frameworks, no build step, no dependencies. Just static files. Fonts load from Google Fonts (requires internet the first time; cached after).

## License

MIT — do whatever you like with it.
