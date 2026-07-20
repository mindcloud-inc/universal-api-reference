# Shotstack: Native API Reference

A consolidated summary of Shotstack's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://shotstack.io/docs/api/
- **API base URL:** `https://api.shotstack.io`

## Authentication

### API Key

Connect Shotstack with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://shotstack.io/docs/guide/getting-started/request-api-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | `POST /edit/v1/templates` | [docs](https://shotstack.io/docs/api/#create-template) |
| [Delete Asset](actions/delete-asset.md) | `DELETE /serve/v1/assets/:id` | [docs](https://shotstack.io/docs/api/#delete-asset) |
| [Delete Source](actions/delete-source.md) | `DELETE /ingest/v1/sources/:id` | [docs](https://shotstack.io/docs/api/#delete-source) |
| [Delete Template](actions/delete-template.md) | `DELETE /edit/v1/templates/:id` | [docs](https://shotstack.io/docs/api/#delete-template) |
| [Direct Upload](actions/direct-upload.md) | `POST /edit/v1/upload` | [docs](https://shotstack.io/docs/api/#direct-upload) |
| [Fetch Source](actions/fetch-source.md) | `POST /ingest/v1/sources` | [docs](https://shotstack.io/docs/api/#fetch-source) |
| [Get Asset](actions/get-asset.md) | `GET /serve/v1/assets/:id` | [docs](https://shotstack.io/docs/api/#get-asset) |
| [Get Asset by Render ID](actions/get-asset-by-render-id.md) | `GET /serve/v1/assets/render/:id` | [docs](https://shotstack.io/docs/api/#get-asset-by-render-id) |
| [Get Render Status](actions/get-render-status.md) | `GET /edit/v1/render/:id` | [docs](https://shotstack.io/docs/api/#get-render-status) |
| [Get Source](actions/get-source.md) | `GET /ingest/v1/sources/:id` | [docs](https://shotstack.io/docs/api/#get-source) |
| [Inspect Media](actions/inspect-media.md) | `GET /edit/v1/probe/:url` | [docs](https://shotstack.io/docs/api/#inspect-media) |
| [List Sources](actions/list-sources.md) | `GET /ingest/v1/sources` | [docs](https://shotstack.io/docs/api/#list-sources) |
| [List Templates](actions/list-templates.md) | `GET /edit/v1/templates` | [docs](https://shotstack.io/docs/api/#list-templates) |
| [Render Asset](actions/render-asset.md) | `POST /edit/v1/render` | [docs](https://shotstack.io/docs/api/#render-asset) |
| [Render Template](actions/render-template.md) | `POST /edit/v1/templates/render` | [docs](https://shotstack.io/docs/api/#render-template) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /edit/v1/templates/:id` | [docs](https://shotstack.io/docs/api/#retrieve-template) |
| [Transfer Asset](actions/transfer-asset.md) | `POST /serve/v1/assets` | [docs](https://shotstack.io/docs/api/#transfer-asset) |
| [Update Template](actions/update-template.md) | `PUT /edit/v1/templates/:id` | [docs](https://shotstack.io/docs/api/#update-template) |
