# NMKR: Native API Reference

A consolidated summary of NMKR's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.nmkr.io/nmkr-studio-api
- **OpenAPI specification:** https://studio-api.nmkr.io/swagger/v2/swagger.json
- **API base URL:** `https://studio-api.nmkr.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.nmkr.io/nmkr-studio-api/get-started-with-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `text/plain` |
| `Content-Type` | `application/json` |

## Pagination

Use `count` in the request parameters to set the page size. Use `page` in the request parameters to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | `GET /v2/ListProjects` | [docs](https://studio-api.nmkr.io/swagger/index.html) |
