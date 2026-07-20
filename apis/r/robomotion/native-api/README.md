# Robomotion: Native API Reference

A consolidated summary of Robomotion's API configuration, with links to official documentation.

- **Official docs:** https://docs.robomotion.io/reference/api/
- **API base URL:** `https://api.robomotion.io`

## Authentication

### API Key

Authenticate with a Robomotion workspace API token. Robomotion requires Authorization: Bearer <token> on every API request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.robomotion.io/reference/api/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `size` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.
