# Kimi: Native API Reference

A consolidated summary of Kimi's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://platform.kimi.ai/docs/api/overview
- **API base URL:** `https://api.moonshot.ai`

## Authentication

### API Key

Authenticate Kimi API requests with a Moonshot API key using bearer authentication.

### Credentials

- **Moonshot API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.kimi.ai/docs/api/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | `GET /v1/users/me/balance` | [docs](https://platform.kimi.ai/docs/api/balance) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://platform.kimi.ai/docs/api/files-list) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://platform.kimi.ai/docs/api/list-models) |
