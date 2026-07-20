# Planado: Native API Reference

A consolidated summary of Planado's API configuration, with links to official documentation.

- **Official docs:** https://api-docs.planadoapp.com/docs/v2/index.html
- **API base URL:** `https://api.planadoapp.com/v2`

## Authentication

### API Key

Use a Planado API key from Settings / Integrations / API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api-docs.planadoapp.com/docs/v2/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `after` in the query string as the pagination cursor.
