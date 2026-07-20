# Fish Audio: Native API Reference

A consolidated summary of Fish Audio's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.fish.audio/api-reference/introduction
- **OpenAPI specification:** https://docs.fish.audio/api-reference/openapi.json
- **API base URL:** `https://api.fish.audio`

## Authentication

### API Key

Use a Fish Audio API key. MindCloud sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fish.audio/developer-guide/sdk-guide/python/authentication)

## Pagination

Use `page_size` in the query string to set the page size (default 10; minimum 1). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | `POST /model` | [docs](https://docs.fish.audio/api-reference/endpoint/model/create-model) |
| [Delete Model](actions/delete-model.md) | `DELETE /model/:id` | [docs](https://docs.fish.audio/api-reference/endpoint/model/delete-model) |
| [Get API Credit](actions/get-api-credit.md) | `GET /wallet/:user_id/api-credit` | [docs](https://docs.fish.audio/api-reference/endpoint/wallet/get-api-credit) |
| [Get Model](actions/get-model.md) | `GET /model/:id` | [docs](https://docs.fish.audio/api-reference/endpoint/model/get-model) |
| [Get User Package](actions/get-user-package.md) | `GET /wallet/:user_id/package` | [docs](https://docs.fish.audio/api-reference/endpoint/wallet/get-user-package) |
| [List Models](actions/list-models.md) | `GET /model` | [docs](https://docs.fish.audio/api-reference/endpoint/model/list-models) |
| [Speech to Text](actions/speech-to-text.md) | `POST /v1/asr` | [docs](https://docs.fish.audio/api-reference/endpoint/openapi-v1/speech-to-text) |
| [Text to Speech](actions/text-to-speech.md) | `POST /v1/tts` | [docs](https://docs.fish.audio/api-reference/endpoint/openapi-v1/text-to-speech) |
| [Update Model](actions/update-model.md) | `PATCH /model/:id` | [docs](https://docs.fish.audio/api-reference/endpoint/model/update-model) |
