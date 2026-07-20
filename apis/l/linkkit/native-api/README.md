# Linkkit: Native API Reference

A consolidated summary of Linkkit's API configuration, with links to official documentation.

- **Official docs:** https://api.uselinkkit.com/docs
- **OpenAPI specification:** https://api.uselinkkit.com/openapi.yaml
- **API base URL:** `https://api.uselinkkit.com`

## Authentication

### API Key

Authenticate Linkkit API requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://uselinkkit.com/help/api-integrations/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The current page number is read from `meta.page`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.
