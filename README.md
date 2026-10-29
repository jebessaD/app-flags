# app-flags

Public remote config for apps (force update, simple flags).

No secrets here — only version gates and public Play Store links.

## Layout

```
<app-id>/app_config.json
```

## Ethio Radio

- File: [`ethio-radio/app_config.json`](ethio-radio/app_config.json)
- Live URL (use this in the app):  
  https://raw.githubusercontent.com/jebessaD/app-flags/main/ethio-radio/app_config.json
- GitHub Pages (optional mirror once built):  
  https://jebessad.github.io/app-flags/ethio-radio/app_config.json

### Force an update

1. Ship the new build to Play.
2. Set `minVersionCode` to that build’s `versionCode` (the `+N` in `1.0.7+8` → `8`).
3. Set `"forceUpdate": true`.
4. Push to `main`.

### Turn off

```json
"forceUpdate": false
```

Or lower `minVersionCode`.

### Add another app

```bash
mkdir my-app
# add my-app/app_config.json
git add -A && git commit -m "Add my-app flags" && git push
```
