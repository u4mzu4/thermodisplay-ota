# ThermoDisplay OTA

Over-the-air update channel for **ThermoDisplay** (`hu.thermodisplay`), the custom thermostat/weather app
running on a rooted Shelly Wall Display gen1.

- **GitHub Releases** — what the display checks: `https://api.github.com/repos/u4mzu4/thermodisplay-ota/releases/latest`.
  The release **tag is the versionCode** (e.g. `31`); the first `.apk` asset is downloaded and installed silently
  (the app runs as a privileged system app).
- **`main` branch** — always carries the current `thermodisplay.apk` and `version.json` too (archive + raw fallback).

APKs here are built **without** baked-in Wi-Fi/Influx credentials, so they contain no secrets.

Publishing (from the app repo): `.\tools\release.ps1 -VersionCode N -VersionName X -Push`.
