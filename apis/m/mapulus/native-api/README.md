# Mapulus: Native API Reference

A consolidated summary of Mapulus's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developer.mapulus.com/v1/docs
- **OpenAPI specification:** https://developer.mapulus.com/v1/openapi.json
- **API base URL:** `https://api.mapulus.com`

## Authentication

### API Key

Use a Mapulus API key with Bearer token authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.mapulus.com/v1/docs#description/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `pages.total_pages`. The current page number is read from `pages.current_page`.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | `POST /api/v1/locations` | [docs](https://developer.mapulus.com/v1/docs) |
| [Delete Location](actions/delete-location.md) | `DELETE /api/v1/locations/:id` | [docs](https://developer.mapulus.com/v1/docs) |
| [Get Location](actions/get-location.md) | `GET /api/v1/locations/:id` | [docs](https://developer.mapulus.com/v1/docs) |
| [Get Map](actions/get-map.md) | `GET /api/v1/maps/:id` | [docs](https://developer.mapulus.com/v1/docs) |
| [List Locations](actions/list-locations.md) | `GET /api/v1/locations` | [docs](https://developer.mapulus.com/v1/docs) |
| [List Maps](actions/list-maps.md) | `GET /api/v1/maps` | [docs](https://developer.mapulus.com/v1/docs) |
| [Update Location](actions/update-location.md) | `PUT /api/v1/locations/:id` | [docs](https://developer.mapulus.com/v1/docs) |
