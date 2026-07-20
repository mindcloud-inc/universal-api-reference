# LightwaveRF Lighting: Native API Reference

A consolidated summary of LightwaveRF Lighting's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api
- **OpenAPI specification:** https://jsapi.apiary.io/apis/linkpluspublicapi.html
- **API base URL:** `https://publicapi.lightwaverf.com/`

## Authentication

### Access Token

Use a LightwaveRF bearer access token from Settings > API Integration > Get Token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://lwtokens.docs.apiary.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Device](actions/add-device.md) | `POST /v1/device/add` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Add LinkPlus](actions/add-link-plus.md) | `POST /v1/linkplus/add` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Batch Read Features](actions/batch-read-features.md) | `POST /v1/features/read` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Batch Read Historical Data](actions/batch-read-historical-data.md) | `POST /v1/data` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Batch Write Features](actions/batch-write-features.md) | `POST /v1/features/write` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Create Room](actions/create-room.md) | `POST /v1/room` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/events` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Create Zone](actions/create-zone.md) | `POST /v1/zone` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Delete Device](actions/delete-device.md) | `DELETE /v1/device/delete/{deviceId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Delete Room](actions/delete-room.md) | `DELETE /v1/room/{roomId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/events/{eventId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Delete Zone](actions/delete-zone.md) | `DELETE /v1/zone/{zoneId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Favourite](actions/get-favourite.md) | `GET /v1/favourite/{favouriteId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Feature](actions/get-feature.md) | `GET /v1/feature/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Room](actions/get-room.md) | `GET /v1/room/{roomId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Structure](actions/get-structure.md) | `GET /v1/structure/{structureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get User Info](actions/get-user-info.md) | `GET /v1/userinfo` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/events/{eventId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Zone](actions/get-zone.md) | `GET /v1/zone/{zoneId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Favourites](actions/list-favourites.md) | `GET /v1/favourites` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Hierarchy](actions/list-hierarchy.md) | `GET /v1/hierarchy` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Rooms](actions/list-rooms.md) | `GET /v1/rooms` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Structures](actions/list-structures.md) | `GET /v1/structures` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/events` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Zones](actions/list-zones.md) | `GET /v1/zones` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Read Historical Data](actions/read-historical-data.md) | `GET /v1/data/{deviceId}/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Set Feature](actions/set-feature.md) | `POST /v1/feature/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Update Favourite](actions/update-favourite.md) | `PUT /v1/favourite/{favouriteId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Update Room](actions/update-room.md) | `PUT /v1/room/{roomId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /v1/events/{eventId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Update Zone](actions/update-zone.md) | `PUT /v1/zone/{zoneId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
