# TLY Link Shortener: Native API Reference

A consolidated summary of TLY Link Shortener's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://t.ly/docs
- **API base URL:** `https://api.t.ly`

## Authentication

### API Key

Connect with a T.LY API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://t.ly/help/integrations/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `limit` in the query string to set the page size (default 30; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Shorten Links](actions/bulk-shorten-links.md) | `POST /api/v1/link/bulk` | [docs](https://t.ly/docs) |
| [Bulk Update Links](actions/bulk-update-links.md) | `POST /api/v1/link/bulk/update` | [docs](https://t.ly/docs) |
| [Create Pixel](actions/create-pixel.md) | `POST /api/v1/link/pixel` | [docs](https://t.ly/docs) |
| [Create Short Link](actions/create-short-link.md) | `POST /api/v1/link/shorten` | [docs](https://t.ly/docs) |
| [Create Tag](actions/create-tag.md) | `POST /api/v1/link/tag` | [docs](https://t.ly/docs) |
| [Create UTM Preset](actions/create-utm-preset.md) | `POST /api/v1/link/utm-preset` | [docs](https://t.ly/docs) |
| [Delete OneLink Stats](actions/delete-one-link-stats.md) | `DELETE /api/v1/onelink/stat` | [docs](https://t.ly/docs) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /api/v1/link/pixel/:id` | [docs](https://t.ly/docs) |
| [Delete Short Link](actions/delete-short-link.md) | `DELETE /api/v1/link` | [docs](https://t.ly/docs) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v1/link/tag/:id` | [docs](https://t.ly/docs) |
| [Delete UTM Preset](actions/delete-utm-preset.md) | `DELETE /api/v1/link/utm-preset/:id` | [docs](https://t.ly/docs) |
| [Expand Short Link](actions/expand-short-link.md) | `POST /api/v1/link/expand` | [docs](https://t.ly/docs) |
| [Get OneLink Stats](actions/get-one-link-stats.md) | `GET /api/v1/onelink/stats` | [docs](https://t.ly/docs) |
| [Get Pixel](actions/get-pixel.md) | `GET /api/v1/link/pixel/:id` | [docs](https://t.ly/docs) |
| [Get QR Code](actions/get-qr-code.md) | `GET /api/v1/link/qr-code` | [docs](https://t.ly/docs) |
| [Get Short Link](actions/get-short-link.md) | `GET /api/v1/link` | [docs](https://t.ly/docs) |
| [Get Short Link Stats](actions/get-short-link-stats.md) | `GET /api/v1/link/stats` | [docs](https://t.ly/docs) |
| [Get Tag](actions/get-tag.md) | `GET /api/v1/link/tag/:id` | [docs](https://t.ly/docs) |
| [Get UTM Preset](actions/get-utm-preset.md) | `GET /api/v1/link/utm-preset/:id` | [docs](https://t.ly/docs) |
| [List OneLinks](actions/list-one-links.md) | `GET /api/v1/onelink/list` | [docs](https://t.ly/docs) |
| [List Pixels](actions/list-pixels.md) | `GET /api/v1/link/pixel` | [docs](https://t.ly/docs) |
| [List Short Links](actions/list-short-links.md) | `GET /api/v1/link/list` | [docs](https://t.ly/docs) |
| [List Tags](actions/list-tags.md) | `GET /api/v1/link/tag` | [docs](https://t.ly/docs) |
| [List UTM Presets](actions/list-utm-presets.md) | `GET /api/v1/link/utm-preset` | [docs](https://t.ly/docs) |
| [Update Pixel](actions/update-pixel.md) | `PUT /api/v1/link/pixel/:id` | [docs](https://t.ly/docs) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /api/v1/link/qr-code` | [docs](https://t.ly/docs) |
| [Update Short Link](actions/update-short-link.md) | `PUT /api/v1/link` | [docs](https://t.ly/docs) |
| [Update Tag](actions/update-tag.md) | `PUT /api/v1/link/tag/:id` | [docs](https://t.ly/docs) |
| [Update UTM Preset](actions/update-utm-preset.md) | `PUT /api/v1/link/utm-preset/:id` | [docs](https://t.ly/docs) |
