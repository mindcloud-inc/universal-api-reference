# Exact Mails: Native API Reference

A consolidated summary of Exact Mails's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://exactmail-dashboard.vercel.app/documentation
- **OpenAPI specification:** https://exactmails.xyz:8012/openapi.json
- **API base URL:** `https://exactmails.xyz:8012`

## Authentication

### API Key

Use your Exact Mails API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://exactmail-dashboard.vercel.app/documentation)

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
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/email/me` | [docs](https://exactmail-dashboard.vercel.app/documentation) |
