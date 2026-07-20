# AgentQL: Native API Reference

A consolidated summary of AgentQL's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://docs.agentql.com/rest-api/api-reference
- **OpenAPI specification:** https://api.agentql.com/openapi.json
- **API base URL:** `https://api.agentql.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.agentql.com/rest-api/api-reference)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Remote Browser Session](actions/create-remote-browser-session.md) | `POST /v1/tetra/sessions` | [docs](https://docs.agentql.com/rest-api/api-reference) |
| [Get Usage](actions/get-usage.md) | `GET /v1/usage` | [docs](https://docs.agentql.com/rest-api/api-reference) |
| [List Session Usage](actions/list-session-usage.md) | `GET /v1/tetra/usage` | [docs](https://docs.agentql.com/rest-api/api-reference) |
| [Query Data](actions/query-data.md) | `POST /v1/query-data` | [docs](https://docs.agentql.com/rest-api/api-reference) |
| [Query Document](actions/query-document.md) | `POST /v1/query-document` | [docs](https://docs.agentql.com/rest-api/api-reference) |
