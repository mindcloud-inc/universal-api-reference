# TikTok Conversions: Native API Reference

A consolidated summary of TikTok Conversions's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://business-api.tiktok.com/portal/docs?id=1740963089558529
- **API base URL:** `https://business-api.tiktok.com`

## Authentication

### Pixel Access Token

Use a TikTok Pixel ID and Events API access token.

### Credentials

- **Access Token:** `accessToken` · required · TikTok Events API access token from Events Manager Settings.
- **Pixel ID:** `pixelId` · required · TikTok Pixel ID from Events Manager.

Send these headers with each API request:

```http
Access-Token: <accessToken>
```

[Official authentication documentation](https://ads.tiktok.com/help/article/events-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Offline Events](actions/batch-offline-events.md) | `POST /open_api/v1.3/offline/batch/` | [docs](https://business-api.tiktok.com/portal/docs?id=1758428053652482) |
| [Batch Pixel Events](actions/batch-pixel-events.md) | `POST /open_api/v1.3/pixel/batch/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858565852225) |
| [Create CRM Event Set](actions/create-crm-event-set.md) | `POST /open_api/v1.3/crm/create/` | [docs](https://business-api.tiktok.com/portal/docs?id=1858830704718658) |
| [Create Offline Event Set](actions/create-offline-event-set.md) | `POST /open_api/v1.3/offline/create/` | [docs](https://business-api.tiktok.com/portal/docs?id=1758427576470529) |
| [Create Pixel](actions/create-pixel.md) | `POST /open_api/v1.3/pixel/create/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858779758593) |
| [Create Pixel Event](actions/create-pixel-event.md) | `POST /open_api/v1.3/pixel/event/create/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858807646209) |
| [Delete Offline Event Set](actions/delete-offline-event-set.md) | `POST /open_api/v1.3/offline/delete/` | [docs](https://business-api.tiktok.com/portal/docs?id=1765596790860802) |
| [Delete Pixel Event](actions/delete-pixel-event.md) | `POST /open_api/v1.3/pixel/event/delete/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858862104578) |
| [Track Event](actions/track-event.md) | `POST /open_api/v1.3/event/track/` | [docs](https://business-api.tiktok.com/portal/docs?id=1771101303285761) |
| [Track Offline Event](actions/track-offline-event.md) | `POST /open_api/v1.3/offline/track/` | [docs](https://business-api.tiktok.com/portal/docs?id=1758428013689857) |
| [Track Pixel Event](actions/track-pixel-event.md) | `POST /open_api/v1.3/pixel/track/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858531237890) |
| [Update Offline Event Set](actions/update-offline-event-set.md) | `POST /open_api/v1.3/offline/update/` | [docs](https://business-api.tiktok.com/portal/docs?id=1765596741157889) |
| [Update Pixel](actions/update-pixel.md) | `POST /open_api/v1.3/pixel/update/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858799524865) |
| [Update Pixel Event](actions/update-pixel-event.md) | `POST /open_api/v1.3/pixel/event/update/` | [docs](https://business-api.tiktok.com/portal/docs?id=1740858823774210) |
