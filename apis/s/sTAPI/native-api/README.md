# STAPI: Native API Reference

A consolidated summary of STAPI's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://stapi.co/api-documentation
- **API base URL:** `https://stapi.co/api`

## Authentication

### No authentication

STAPI public REST API requires no credentials.

This API does not require request authentication.

[Official authentication documentation](https://stapi.co/api-overview)

## Pagination

Use `pageSize` in the query string to set the page size (default 10; minimum 1). Use `pageNumber` in the query string to choose the page; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | `GET /v1/rest/character` | [docs](https://stapi.co/api-documentation) |
| [Get Episode](actions/get-episode.md) | `GET /v1/rest/episode` | [docs](https://stapi.co/api-documentation) |
| [Get Performer](actions/get-performer.md) | `GET /v2/rest/performer` | [docs](https://stapi.co/api-documentation) |
| [Get Series](actions/get-series.md) | `GET /v1/rest/series` | [docs](https://stapi.co/api-documentation) |
| [Search Characters](actions/search-characters.md) | `POST /v1/rest/character/search` | [docs](https://stapi.co/api-documentation) |
| [Search Episodes](actions/search-episodes.md) | `POST /v1/rest/episode/search` | [docs](https://stapi.co/api-documentation) |
| [Search Performers](actions/search-performers.md) | `POST /v2/rest/performer/search` | [docs](https://stapi.co/api-documentation) |
| [Search Series](actions/search-series.md) | `POST /v1/rest/series/search` | [docs](https://stapi.co/api-documentation) |
