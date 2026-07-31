# DiceBear: Native API Reference

A consolidated summary of DiceBear's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.dicebear.com/how-to-use/http-api
- **API base URL:** `https://api.dicebear.com/10.x`

## Authentication

### No Authentication

Public HTTP API access with no authentication required.

This API does not require request authentication.

[Official authentication documentation](https://www.dicebear.com/how-to-use/http-api/)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Adventurer Avatar](actions/generate-adventurer-avatar.md) | `GET /adventurer/svg` | [docs](https://www.dicebear.com/styles/adventurer/) |
| [Generate Adventurer Neutral Avatar](actions/generate-adventurer-neutral-avatar.md) | `GET /adventurer-neutral/svg` | [docs](https://www.dicebear.com/styles/adventurer-neutral/) |
| [Generate Avataaars Avatar](actions/generate-avataaars-avatar.md) | `GET /avataaars/svg` | [docs](https://www.dicebear.com/styles/avataaars/) |
| [Generate Avataaars Neutral Avatar](actions/generate-avataaars-neutral-avatar.md) | `GET /avataaars-neutral/svg` | [docs](https://www.dicebear.com/styles/avataaars-neutral/) |
| [Generate Avatar Image](actions/generate-avatar-image.md) | `GET /:styleName/:format` | [docs](https://www.dicebear.com/how-to-use/http-api) |
| [Generate Bottts Avatar](actions/generate-bottts-avatar.md) | `GET /bottts/svg` | [docs](https://www.dicebear.com/styles/bottts/) |
| [Generate Bottts Neutral Avatar](actions/generate-bottts-neutral-avatar.md) | `GET /bottts-neutral/svg` | [docs](https://www.dicebear.com/styles/bottts-neutral/) |
| [Generate Icons Avatar](actions/generate-icons-avatar.md) | `GET /icons/svg` | [docs](https://www.dicebear.com/styles/icons/) |
| [Generate Identicon Avatar](actions/generate-identicon-avatar.md) | `GET /identicon/svg` | [docs](https://www.dicebear.com/styles/identicon/) |
| [Generate Initials Avatar](actions/generate-initials-avatar.md) | `GET /initials/svg` | [docs](https://www.dicebear.com/styles/initials/) |
| [Generate Lorelei Avatar](actions/generate-lorelei-avatar.md) | `GET /lorelei/svg` | [docs](https://www.dicebear.com/styles/lorelei/) |
| [Generate Lorelei Neutral Avatar](actions/generate-lorelei-neutral-avatar.md) | `GET /lorelei-neutral/svg` | [docs](https://www.dicebear.com/styles/lorelei-neutral/) |
| [Generate Open Peeps Avatar](actions/generate-open-peeps-avatar.md) | `GET /open-peeps/svg` | [docs](https://www.dicebear.com/styles/open-peeps/) |
| [Generate Personas Avatar](actions/generate-personas-avatar.md) | `GET /personas/svg` | [docs](https://www.dicebear.com/styles/personas/) |
| [Generate Pixel Art Avatar](actions/generate-pixel-art-avatar.md) | `GET /pixel-art/svg` | [docs](https://www.dicebear.com/styles/pixel-art/) |
| [Generate Pixel Art Neutral Avatar](actions/generate-pixel-art-neutral-avatar.md) | `GET /pixel-art-neutral/svg` | [docs](https://www.dicebear.com/styles/pixel-art-neutral/) |
| [Generate Rings Avatar](actions/generate-rings-avatar.md) | `GET /rings/svg` | [docs](https://www.dicebear.com/styles/rings/) |
| [Generate Shapes Avatar](actions/generate-shapes-avatar.md) | `GET /shapes/svg` | [docs](https://www.dicebear.com/styles/shapes/) |
| [Generate Thumbs Avatar](actions/generate-thumbs-avatar.md) | `GET /thumbs/svg` | [docs](https://www.dicebear.com/styles/thumbs/) |
| [Get Avatar Metadata](actions/get-avatar-metadata.md) | `GET /:styleName/json` | [docs](https://www.dicebear.com/how-to-use/http-api/) |
| [Get Style Definition](actions/get-style-definition.md) | `GET /:styleName/definition.json` | [docs](https://www.dicebear.com/how-to-use/http-api) |
| [Get Style Options](actions/get-style-options.md) | `GET /:styleName/options.json` | [docs](https://www.dicebear.com/how-to-use/http-api) |
| [List Avatar Styles](actions/list-avatar-styles.md) | `GET /` | [docs](https://www.dicebear.com/how-to-use/http-api) |
