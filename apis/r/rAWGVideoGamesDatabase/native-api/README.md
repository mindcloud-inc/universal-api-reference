# RAWG Video Games Database: Native API Reference

A consolidated summary of RAWG Video Games Database's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://rawg.io/apidocs
- **OpenAPI specification:** https://api.rawg.io/docs/?format=openapi
- **API base URL:** `https://api.rawg.io/api`

## Authentication

### API Key

Use your RAWG API key. MindCloud stores it as credentials.apiKey and injects it into the shared query parameter key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rawg.io/apidocs)

## Pagination

Use `page_size` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Games](actions/list-games.md) | `GET /games` | [docs](https://api.rawg.io/docs/) |
