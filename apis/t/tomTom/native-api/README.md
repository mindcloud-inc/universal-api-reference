# TomTom: Native API Reference

A consolidated summary of TomTom's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developer.tomtom.com/documentation
- **API base URL:** `https://api.tomtom.com`

## Authentication

### TomTom API Key

Store the TomTom API key and inject it into provider-specific request shapes such as the shared `key` query parameter.

### Credentials

- **API Key:** `apiKey` · required · TomTom API key from the project dashboard. Stored once and reused for query or header injection depending on the endpoint family.

[Official authentication documentation](https://developer.tomtom.com/documentation)

## API conventions

Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `ofs` in the query string as the record offset; numbering starts at 0.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List POI Categories](actions/list-poi-categories.md) | `GET /search/2/poiCategories.json` | [docs](https://developer.tomtom.com/search-api/documentation/poi-categories-service/poi-categories) |
