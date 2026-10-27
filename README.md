# Hypersense Ultimate

A non-root Android performance script for **Free Fire, Free Fire Max and PES**, built around one idea: the game gets the resources, everything else waits.

Auto-detects the game in the foreground, scales touch and frame rate to it, and backs off when the battery or the thermal sensor says stop.

## Features

- **Auto game detection** &mdash; starts tuning when a supported title comes forward
- **Adaptive Frame Booster (AFB)** &mdash; frame pacing with FPS history smoothing
- **Dynamic touch scaling** &mdash; X and Y response tuned per title
- **Network priority** &mdash; foreground traffic first, for lower multiplayer latency
- **Battery and thermal AI** &mdash; reduces the profile before the device throttles itself
- **VRAM simulation** &mdash; a managed swap region for spikes
- **Logging** &mdash; FPS, latency and battery written to `hypersense_perf_log.txt`

## Run

```bash
pkg install -y git
git clone https://github.com/hypersenseindia/Hypersense-Ultimate
cd Hypersense-Ultimate
chmod +x hypersense_ultimate.sh
./hypersense_ultimate.sh
```

## State files

```
~/.hypersense_config          saved settings
~/.hypersense_activation      activation state
~/.hypersense_fps_history     rolling FPS samples (window: 5)
hypersense_perf_log.txt       performance log
```

## Notes

- Non-root. Nothing is written to `/system`.
- The log file is plain text and grows; delete it periodically.
- Gains are device-dependent. A phone already at its thermal limit will throttle regardless of any script.
---

<p align="center">
  <sub>Built by <b>AG HYDRAXFF</b> &mdash; HYPERSENSEGLOBAL &middot;
  <a href="https://www.instagram.com/hydraxff_yt/">@hydraxff_yt</a></sub>
</p>