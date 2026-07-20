# GNews: Native API Reference

A consolidated summary of GNews's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.gnews.io
- **API base URL:** `https://gnews.io/api/v4`

## Authentication

### API Key

Authenticate with your GNews API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.gnews.io/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `articles`.

## Pagination

Use `max` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Top Headlines](actions/list-top-headlines.md) | `GET /top-headlines` | [docs](https://docs.gnews.io/endpoints/top-headlines-endpoint) |
| [Search Articles](actions/search-articles.md) | `GET /search` | [docs](https://docs.gnews.io/endpoints/search-endpoint) |
