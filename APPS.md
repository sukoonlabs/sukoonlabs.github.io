# apps.json

The "More apps" list shown inside every Sukoon Labs game. Served at
https://sukoonlabs.github.io/apps.json once merged to `main`.

Fields per app:
- `id`: stable slug. Each game hides the entry with its own id.
- `name`, `tagline` (under 90 characters), `category`.
- `icon`: absolute URL to a square PNG, 256 px or larger, kept in this repo. `null` shows a placeholder.
- `status`: `live` (has a store link) or `coming_soon` (shown without a Get button).
- `order`: lower numbers show first.
- `ios`: `{ "appId": "...", "url": "https://apps.apple.com/app/id..." }` or `null`.
- `android`: `{ "package": "...", "url": "https://play.google.com/store/apps/details?id=..." }` or `null`.

Rules: bump `version` only for breaking shape changes; update `updated` on every edit. Apps cache the last good copy and fall back to it offline.
