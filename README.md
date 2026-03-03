# Painel Nano

Public repository for Painel Nano release management.

## What is in this repo

- `config/remote_config.json`: remote links and update metadata consumed by the app.
- Release tags and changelogs.
- Documentation for update flow.

## Remote config URL used by app

The app fetches this file at runtime:

`https://raw.githubusercontent.com/DouglasReisofc/painelnano/main/config/remote_config.json`

Fallback URL (CDN mirror):

`https://cdn.jsdelivr.net/gh/DouglasReisofc/painelnano@main/config/remote_config.json`

## Remote config schema

```json
{
  "links": {
    "tiktok": "https://www.tiktok.com/@youruser",
    "instagram": "https://www.instagram.com/youruser/",
    "whatsapp_channel": "https://whatsapp.com/channel/..."
  },
  "update": {
    "version_code": 1250,
    "version_name": "2.5",
    "version_notes": "What changed in this version",
    "update_url": "https://github.com/DouglasReisofc/painelnano/releases"
  }
}
```

## How the in-app update check works

- App compares local `versionCode` with `update.version_code` from JSON.
- If remote is greater, the app shows update state in the top-right menu (bell/update action).
- Clicking the update action opens `update.update_url`.
- If remote fetch fails, app uses local fallback URLs and does not crash.

## Social links behavior

Social buttons read URLs from remote config keys:

- `links.tiktok`
- `links.instagram`
- `links.whatsapp_channel`

This means you can change social links without shipping a new APK.

## Release workflow

1. Build and publish a new APK.
2. Create GitHub release and upload APK.
3. Update `config/remote_config.json`:
   - increase `update.version_code`
   - update `version_name`
   - update `version_notes`
   - ensure `update_url` points to release page
4. Commit and push to `main`.
5. App users will receive update signal automatically.

## Notes

- Keep `version_code` numeric and always increasing.
- Keep JSON valid (no trailing commas).
- Prefer updating links via this file instead of hardcoding in app.
