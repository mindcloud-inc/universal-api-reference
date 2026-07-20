# Builder.io: Native API Reference

A consolidated summary of Builder.io's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.builder.io/c/docs/api-intro
- **API base URL:** `https://cdn.builder.io`

## Authentication

### API Key

Use a Builder private API key for Admin, Write, and Upload API requests.

### Credentials

- **API Key:** `apiKey` · required
- **Public API Key:** `publicApiKey` · required · Builder public API key used for Content API read requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.builder.io/c/docs/using-your-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Models](actions/list-models.md) | `POST api/v2/admin` | [docs](https://www.builder.io/c/docs/admin-api) |
