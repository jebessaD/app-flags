# app-flags

Public remote config for apps (force update, simple flags).

No secrets here — only version gates and public Play Store links.

## Layout

```
<app-id>/app_config.json
```

## Ethio Radio

- File: [`ethio-radio/app_config.json`](ethio-radio/app_config.json)
- URL: https://jebessad.github.io/app-flags/ethio-radio/app_config.json

### Force an update

1. Ship the new build to Play.
2. Set `minVersionCode` to that build’s `versionCode` (the `+N` in `1.0.7+8` → `8`).
3. Set `"forceUpdate": true`.
4. Push to `main` — GitHub Pages updates in about a minute.

### Turn off

```json
"forceUpdate": false
```

Or lower `minVersionCode`.
