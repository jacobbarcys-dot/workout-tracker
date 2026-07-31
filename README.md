# Lite Workout Tracker

A Hevy-style workout tracker in a single HTML file. No build step, no backend,
no account. Open it and train.

All data is stored locally in your browser (`localStorage`), so it works offline
and never leaves your device.

## Use it

Download `index.html` and open it in any browser. On a phone, open it in the
mobile browser and use **Add to Home Screen** for a full-screen, app-like feel.

## Features

**Workouts**
- Start an empty workout or launch a saved routine from Home or Routines
- A running workout takes over the screen with its own live timer. Collapse it
  with the ▾ and it shrinks to a bar above the tab bar, so you can browse the
  rest of the app mid-session; tap the bar to go full screen again. The
  collapsed state survives a reload
- Live duration, volume, and set counters
- Per-set logging with a checkmark; completed rows highlight green
- **Sets arrive pre-filled** — last session's actual numbers win, and on a
  routine's first run its target fills in (a `3-5` range seeds 3)
- **Swap an exercise mid-workout** — each routine exercise can carry
  alternatives ("or incline walk", "or lat pulldown"). Tap ⇄ to switch; the set
  count and targets carry over, and the table reshapes if the new exercise is
  measured differently
- Tap a set number for its menu — switch it to a **warmup set** ("W", excluded
  from volume, set counts, and PRs) or **delete the set**
- Rest timer auto-starts after each completed set (90s default, ±15s, skip)
- Every destructive action (discard, delete, replace) asks first in an in-app
  confirmation popup that names exactly what will be lost

**Five ways to track a set**
Each exercise declares how it's measured, and the set table adapts:

| Mode | Used for |
|---|---|
| Weight × reps | Barbell and dumbbell lifts |
| Reps only | Bodyweight work, plyos, mobility reps |
| Weight × time | Loaded carries |
| Time only | Planks, holds, stretches |
| Minutes | Cardio, Zone 2, intervals |

**Home**
- Greeting, week streak, hours trained this week, and bodyweight
- **Deload clock** — tracks what training week you're on against a 4/5/6-week
  cycle, warns when a deload is due or overdue, and resets when you log one
- One-tap start for today's session from whichever folder is your current split
- Resume banner when a workout is in progress

**Routines**
- Each exercise holds real sets with **target rep ranges** (`3-5`, `8-12`) or
  time/minute targets, prefilled when you start the routine
- **Circuits/rounds** — grouped exercises are wrapped in a round box. One round
  is one set of *each* exercise in the box, then back to the top; set numbers
  read R1/R2/R3, a counter tracks "Round 2 of 4", and one button adds a round
  to every exercise at once
- **Per-exercise notes** for cues ("per side") and a list of swappable alternatives
- Assign a **day of the week** and free-form routine notes
- Organize routines into folders, with folder-level notes for progression rules

**History**
- Every finished workout with duration, volume, and sets
- Tap through for the full set breakdown; repeat or delete
- New personal records flagged on the finish screen (Epley estimated 1RM)

**Exercises**
- ~90 exercises seeded — lifts, plyos, carries, mobility, and cardio —
  searchable and filterable by muscle group
- Add your own custom exercises, choosing how they're tracked
- Per-exercise detail: best set, estimated 1RM, and a progress chart over time

## Notes

- Weights are in **lbs**.
- Data lives in `localStorage` under the key `lift.db.v1`, which is per-browser
  and per-device. Clearing site data wipes your history — an export/backup
  button is the next planned feature.

## License

MIT
