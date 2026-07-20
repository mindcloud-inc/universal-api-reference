# SEA-LION AI Playground: Native API Reference

A consolidated summary of SEA-LION AI Playground's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.sea-lion.ai/guides/inferencing/api
- **OpenAPI specification:** https://api.sea-lion.ai/openapi.json
- **API base URL:** `https://api.sea-lion.ai/v1`

## Authentication

### API Key

Connect to SEA-LION with a tenant API key from the SEA-LION Playground.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.sea-lion.ai/guides/inferencing/api)

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
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/completions` | [docs](https://docs.sea-lion.ai/guides/inferencing/api) |
| [Create Embedding](actions/create-embedding.md) | `POST /embeddings` | [docs](https://api.sea-lion.ai/openapi.json) |
| [Create Response](actions/create-response.md) | `POST /responses` | [docs](https://api.sea-lion.ai/openapi.json) |
| [Create Text Completion](actions/create-text-completion.md) | `POST /completions` | [docs](https://api.sea-lion.ai/openapi.json) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://docs.sea-lion.ai/guides/inferencing/api) |
| [Rerank Documents](actions/rerank-documents.md) | `POST /rerank` | [docs](https://api.sea-lion.ai/openapi.json) |
