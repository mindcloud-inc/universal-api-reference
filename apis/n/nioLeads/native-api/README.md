# NioLeads: Native API Reference

A consolidated summary of NioLeads's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://nioleads.com/apidoc/
- **API base URL:** `https://v2.nioleads.com/api/openapi`

## Authentication

### API Key

Authenticate NioLeads requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://nioleads.com/apidoc/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | `POST /find_email` | [docs](https://nioleads.com/apidoc/#email-finder) |
| [Get Credits](actions/get-credits.md) | `GET /credits` | [docs](https://nioleads.com/apidoc/#get-credits) |
