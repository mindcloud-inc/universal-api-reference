# Vercel AI Gateway Chat Model: Native API Reference

A consolidated summary of Vercel AI Gateway Chat Model's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://vercel.com/docs/ai-gateway
- **API base URL:** `https://ai-gateway.vercel.sh/v1`

## Authentication

### API Key

Connect with a Vercel AI Gateway API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://vercel.com/docs/ai-gateway/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://vercel.com/docs/ai-gateway/capabilities/usage) |
| [Get Model](actions/get-model.md) | `GET /models/:model` | [docs](https://vercel.com/docs/ai-gateway/openai-compat) |
| [Get Model Endpoints](actions/get-model-endpoints.md) | `GET /models/:creator/:model/endpoints` | [docs](https://vercel.com/docs/ai-gateway/models-and-providers/) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://vercel.com/docs/ai-gateway/sdks-and-apis/openai-compat/rest-api) |
