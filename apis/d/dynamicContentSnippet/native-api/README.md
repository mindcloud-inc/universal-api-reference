# Dynamic Content Snippet: Native API Reference

A consolidated summary of Dynamic Content Snippet's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://contentsnip.com/documentation.htm
- **API base URL:** `https://app.contentsnip.com`

## Authentication

### API Key

Authenticate ContentSnip API requests with the provider API key in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://contentsnip.com/documentation.htm)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update URL Mapping](actions/create-or-update-url-mapping.md) | `POST /api/mappings` | [docs](https://contentsnip.com/documentation.htm) |
| [Retrieve URL Mappings](actions/retrieve-url-mappings.md) | `GET /api/mappings` | [docs](https://contentsnip.com/documentation.htm) |
