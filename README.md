# Video Player

Standalone, 100% offline Android video player (no INTERNET permission).
Original code written for this project — MX Player–style feature set, no
copied code, assets or branding.

- Package: `com.mylock.videoplayer`
- compileSdk / targetSdk: **35 (Android 15)**, minSdk 26
- Kotlin + AndroidX Media3 (ExoPlayer) 1.4.1

## Features

- Library from MediaStore: All Videos + Folders tabs, thumbnails,
  name / duration / resolution / size on every row, search, sort
  (name / date / duration / size)
- Favorites (★) and Recently Played tabs
- Player: fullscreen landscape, tap to show/hide controls, play/pause,
  seek bar, next/previous in the current list, speed 0.5×–2×,
  subtitle track select, load external subtitle file (.srt/.vtt/.ass/.ttml),
  audio track select, screen lock, aspect/resize modes (Fit/Fill/Zoom)
- Gestures: left vertical swipe = brightness, right vertical swipe = volume,
  horizontal swipe = seek, double-tap sides = −10s / +10s, on-screen indicator
- Resume: per-video position memory with resume indicator in the library
- Picture-in-Picture (button + on leaving the app while playing)
- Midnight dark theme, Android 15 edge-to-edge handling
- Built-in SelfTest screen (logcat tag `VPTEST`, SUMMARY line)

## Build

Push `VideoPlayer.zip` (project source) plus this README and
`.github/workflows/build.yml` to the repo root — GitHub Actions unzips the
project and builds the debug APK, published as the **VideoPlayer-APK**
artifact. The `autotest` job then runs the built-in SelfTest on an
Android 15 (API 35) emulator.
