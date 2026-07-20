# Melo: Native API Reference

A consolidated summary of Melo's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.melo.io/api-reference/concepts
- **API base URL:** `https://preprod-api.notif.immo`

## Authentication

### API Key Header

Authenticate Melo requests using only the X-API-KEY header without bearer authorization.

### Credentials

- **API Key:** `apiKey` · required · Melo API key value used in X-API-KEY header.

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.melo.io/api-reference/faq)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `itemsPerPage` in the query string to set the page size (default 10; accepted range 0–30). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Search](actions/create-search.md) | `POST /searches` | [docs](https://docs.melo.io/api-reference/endpoint/searches/create) |
| [Delete Search](actions/delete-search.md) | `DELETE /searches/:id` | [docs](https://docs.melo.io/api-reference/endpoint/searches/delete) |
| [Get Search](actions/get-search.md) | `GET /searches/:id` | [docs](https://docs.melo.io/api-reference/endpoint/searches/get_single) |
| [List Cities](actions/list-cities.md) | `GET /cities` | [docs](https://docs.melo.io/api-reference/endpoint/indicators/cities) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://docs.melo.io/api-reference/concepts) |
| [List Points of Interest](actions/list-points-of-interest.md) | `GET /indicators/points_of_interest` | [docs](https://docs.melo.io/api-reference/endpoint/indicators/points_of_interest) |
| [List Searches](actions/list-searches.md) | `GET /searches` | [docs](https://docs.melo.io/api-reference/endpoint/searches/get_collection) |
| [Search Locations](actions/search-locations.md) | `GET /public/location-autocomplete` | [docs](https://docs.melo.io/api-reference/endpoint/indicators/locations) |
| [Update Search](actions/update-search.md) | `PUT /searches/:id` | [docs](https://docs.melo.io/api-reference/endpoint/searches/update) |
