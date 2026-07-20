# SalesViewer: Native API Reference

A consolidated summary of SalesViewer's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://salesviewer.github.io/salesviewer-api/
- **OpenAPI specification:** https://salesviewer.github.io/salesviewer-api/swagger/salesviewer-api.swagger.json
- **API base URL:** `https://api.salesviewer.com/`

## Authentication

### API Key

Use the SalesViewer API key from Projects & Tracking. SalesViewer documents API key usage through the X-SV-APIKEY header and also supports an apiKey query parameter fallback.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-SV-APIKEY: <apiKey>
```

[Official authentication documentation](https://www.salesviewer.com/en/help/integrations/salesviewer-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`. The current page number is read from `pagination.current`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Sessions](actions/search-sessions.md) | `GET /sessions.json` | [docs](https://salesviewer.github.io/salesviewer-api/definition) |
| [Search Sessions by Form Data](actions/search-sessions-by-form-data.md) | `POST /sessions.json` | [docs](https://salesviewer.github.io/salesviewer-api/definition) |
