# Lift — Workout Tracker

A Hevy-style workout tracker in a single HTML file. No build step, no backend,
no account. Open it and train.

All data is stored locally in your browser (`localStorage`), so it works offline
and never leaves your device.

## Use it

Download `index.html` and open it in any browser. On a phone, open it in the
mobile browser and use **Add to Home Screen** for a full-screen, app-like feel.

## Features

**Workouts**
- Start an empty workout or launch a saved routine
- Live duration, volume, and set counters
- Per-set weight × reps logging with a checkmark; completed rows highlight green
- Your previous session's numbers show as ghost values — tap ✓ on an empty set
  and they auto-fill
- Tap a set number to toggle it to a **warmup set** ("W"). Warmups are excluded
  from volume, set counts, and PRs
- Rest timer auto-starts after each completed set (90s default, ±15s, skip)

**Routines**
- Reusable templates where each exercise holds real sets with target weight ×
  reps, prefilled when you start the routine
- Organize routines into folders (e.g. Push Pull Legs)

**History**
- Every finished workout with duration, volume, and sets
- Tap through for the full set breakdown; repeat or delete
- New personal records flagged on the finish screen (Epley estimated 1RM)

**Exercises**
- ~40 exercises seeded, searchable and filterable by muscle group
- Add your own custom exercises
- Per-exercise detail: best set, estimated 1RM, and a progress chart over time

## Notes

- Weights are in **lbs**.
- Data lives in `localStorage` under the key `lift.db.v1`, which is per-browser
  and per-device. Clearing site data wipes your history — an export/backup
  button is the next planned feature.

## License

MIT
