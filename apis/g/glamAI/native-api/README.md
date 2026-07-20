# Glam AI: Native API Reference

A consolidated summary of Glam AI's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://glam-ai.readme.io/reference/welcome
- **API base URL:** `https://api.glam.ai/api/v1`

## Authentication

### Glam AI API Key

Authenticate Glam AI API requests with an API key sent in the X-API-Key request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://glam-ai.readme.io/reference/welcome)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Generation](actions/create-generation.md) | `POST /generate` | [docs](https://glam-ai.readme.io/reference/generate_generate_post) |
| [Create Try-On Generation](actions/create-try-on-generation.md) | `POST /tryon` | [docs](https://glam-ai.readme.io/reference/generate_tryon_tryon_post) |
| [Get Filters](actions/get-filters.md) | `GET /filters` | [docs](https://glam-ai.readme.io/reference/get_filters_filters_get) |
| [Get Generation Result](actions/get-generation-result.md) | `GET /result/:event_id` | [docs](https://glam-ai.readme.io/reference/get_result_result__event_id__get) |
| [Get Try-On Result](actions/get-try-on-result.md) | `GET /tryon/:event_id` | [docs](https://glam-ai.readme.io/reference/get_result_tryon__event_id__get) |
| [Upload Image](actions/upload-image.md) | `POST /upload` | [docs](https://glam-ai.readme.io/reference/upload_image_upload_post) |
