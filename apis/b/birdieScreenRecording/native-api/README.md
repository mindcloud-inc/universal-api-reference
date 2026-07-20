# Birdie Screen Recording: Native API Reference

A consolidated summary of Birdie Screen Recording's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.birdie.so/birdie-docs/birdie-api
- **API base URL:** `https://app.birdie.so`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.birdie.so/birdie-docs/birdie-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Recordings](actions/list-recordings.md) | `GET /api/v1/videos` | [docs](https://docs.birdie.so/birdie-docs/birdie-api/reference/api-reference/list-recordings) |
