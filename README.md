# 5×4.9

The 5×5 beginner barbell program as an installable, offline phone app.
No account, no server, no tracking — the log lives in the phone's own storage.

**Live:** https://ecalafat.github.io/5x49/

## Install

- **iPhone (iOS 15+)** — open the link in **Safari** → Share → *Add to Home Screen*.
- **Android** — open in **Chrome** → *Install app* (or ⋮ → *Add to Home screen*).

Launch it from the home-screen icon afterwards, not a browser tab. Once loaded it
never needs the network again.

## The program

Two workouts, alternating, three days a week, never two days in a row.

- **A** — Squat 5×5, Bench Press 5×5, Barbell Row 5×5
- **B** — Squat 5×5, Overhead Press 5×5, Deadlift 1×5

Clear all the reps and that lift goes up 2.5 kg next session (deadlift 5 kg). Miss reps
and it repeats. Miss three sessions in a row on one lift and it deloads 10%, rounded to
a weight you can actually load.

The app picks the weights, shows which plates go on each side of the bar, times the
rest, draws a training calendar and tracks bodyweight. Metric by default.

## Backups

There is no cloud. **Settings → Export** writes a JSON file (share sheet on a phone).
On a new phone, tap **Restore a backup** on the first setup screen. Deleting the app
deletes the log, so export occasionally.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app — HTML, CSS and JS in one file. |
| `sw.js` | Service worker; caches everything for offline use. |
| `manifest.webmanifest` | Makes it installable. |
| `icon-*.png` | App icons. |

Editing note: this folder is generated. Sources and the build script live outside the
repo. After changing anything here, bump `CACHE` in `sw.js` so installed phones pick
up the new version instead of serving the old cache.
