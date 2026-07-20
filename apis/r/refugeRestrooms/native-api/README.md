# Refuge Restrooms: Native API Reference

A consolidated summary of Refuge Restrooms's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://www.refugerestrooms.org/api/docs/
- **OpenAPI specification:** https://www.refugerestrooms.org/api/swagger_doc
- **API base URL:** `https://www.refugerestrooms.org/api`

## Authentication

### No authentication

Refuge Restrooms public API endpoints do not require authentication.

This API does not require request authentication.

[Official authentication documentation](https://www.refugerestrooms.org/api/docs/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 2; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Restrooms](actions/list-restrooms.md) | `GET /v1/restrooms` | [docs](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1Restrooms) |
| [Search Restrooms](actions/search-restrooms.md) | `GET /v1/restrooms/search` | [docs](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsSearch) |
| [Search Restrooms by Date](actions/search-restrooms-by-date.md) | `GET /v1/restrooms/by_date` | [docs](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsByDate) |
| [Search Restrooms by Location](actions/search-restrooms-by-location.md) | `GET /v1/restrooms/by_location` | [docs](https://www.refugerestrooms.org/api/docs/#!/restrooms/getV1RestroomsByLocation) |
