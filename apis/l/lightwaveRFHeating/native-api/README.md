# LightwaveRF Heating: Native API Reference

A consolidated summary of LightwaveRF Heating's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://support.lightwaverf.com/knowledge/link-plus-smart-series-api
- **API base URL:** `https://publicapi.lightwaverf.com`

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

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Read Heating Features](actions/batch-read-heating-features.md) | `POST /v1/features/read` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Batch Read Heating Historical Data](actions/batch-read-heating-historical-data.md) | `POST /v1/data` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Batch Write Heating Features](actions/batch-write-heating-features.md) | `POST /v1/features/write` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Heating Feature](actions/get-heating-feature.md) | `GET /v1/feature/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Room](actions/get-room.md) | `GET /v1/room/{roomId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get Structure](actions/get-structure.md) | `GET /v1/structure/{structureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Get User Info](actions/get-user-info.md) | `GET /v1/userinfo` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Heating Hierarchy](actions/list-heating-hierarchy.md) | `GET /v1/hierarchy` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Rooms](actions/list-rooms.md) | `GET /v1/rooms` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [List Structures](actions/list-structures.md) | `GET /v1/structures` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Read Heating Historical Data](actions/read-heating-historical-data.md) | `GET /v1/data/{deviceId}/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
| [Set Heating Feature](actions/set-heating-feature.md) | `POST /v1/feature/{featureId}` | [docs](https://jsapi.apiary.io/apis/linkpluspublicapi.html) |
