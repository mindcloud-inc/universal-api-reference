# HappyScribe: Native API Reference

A consolidated summary of HappyScribe's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://dev.happyscribe.com/sections/product/
- **API base URL:** `https://www.happyscribe.com/api/v1`

## Authentication

### API Key

Use a HappyScribe API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Organization ID:** `organizationId` · required · HappyScribe workspace organization ID used by organization-scoped endpoints such as transcriptions, glossaries, and style guides.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.happyscribe.com/sections/product/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Order](actions/confirm-order.md) | `POST /orders/:id/confirm` | [docs](https://dev.happyscribe.com/sections/product/#orders-confirm-an-order) |
| [Create Export](actions/create-export.md) | `POST /exports` | [docs](https://dev.happyscribe.com/sections/product/#exports-create-an-export) |
| [Create Transcription or Subtitling Order](actions/create-transcription-or-subtitling-order.md) | `POST /orders` | [docs](https://dev.happyscribe.com/sections/product/#orders-create-a-transcription-or-subtitling-order) |
| [Create Translation Order](actions/create-translation-order.md) | `POST /orders/translation` | [docs](https://dev.happyscribe.com/sections/product/#orders-create-a-translation-order) |
| [Delete Transcription](actions/delete-transcription.md) | `DELETE /transcriptions/:id` | [docs](https://dev.happyscribe.com/sections/product/#transcriptions-delete-a-transcription) |
| [Get Signed URL](actions/get-signed-url.md) | `GET /uploads/new` | [docs](https://dev.happyscribe.com/sections/product/#uploads-1-get-a-signed-url) |
| [List Glossaries](actions/list-glossaries.md) | `GET /glossaries` | [docs](https://dev.happyscribe.com/sections/product/#glossaries-list-glossaries) |
| [List Style Guides](actions/list-style-guides.md) | `GET /style_guides` | [docs](https://dev.happyscribe.com/sections/product/#style-guides-list-style-guides) |
| [List Transcriptions](actions/list-transcriptions.md) | `GET /transcriptions` | [docs](https://dev.happyscribe.com/sections/product/#transcriptions-list-all-transcriptions) |
| [Retrieve Export](actions/retrieve-export.md) | `GET /exports/:id` | [docs](https://dev.happyscribe.com/sections/product/#exports-retrieve-an-export) |
| [Retrieve Order](actions/retrieve-order.md) | `GET /orders/:id` | [docs](https://dev.happyscribe.com/sections/product/#orders-retrieve-an-order) |
| [Retrieve Transcription](actions/retrieve-transcription.md) | `GET /transcriptions/:id` | [docs](https://dev.happyscribe.com/sections/product/#transcriptions-retrieve-a-transcription) |
