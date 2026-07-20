# Geocodio: Native API Reference

A consolidated summary of Geocodio's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.geocod.io/docs/
- **OpenAPI specification:** https://api.geocod.io/openapi-spec.json
- **API base URL:** `https://api.geocod.io/v1.12`

## Authentication

### API Key

Use a Geocodio API key for authenticated API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.geocod.io/docs/#authentication)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Geocode Addresses](actions/batch-geocode-addresses.md) | `POST /geocode` | [docs](https://www.geocod.io/docs/#batch-geocoding) |
| [Batch Reverse Geocode Coordinates](actions/batch-reverse-geocode-coordinates.md) | `POST /reverse` | [docs](https://www.geocod.io/docs/#batch-reverse-geocoding) |
| [Calculate Distance From Origin](actions/calculate-distance-from-origin.md) | `GET /distance` | [docs](https://www.geocod.io/docs/#single-origin-distance) |
| [Calculate Distance Matrix](actions/calculate-distance-matrix.md) | `POST /distance-matrix` | [docs](https://www.geocod.io/docs/#distance-matrix) |
| [Create Distance Job](actions/create-distance-job.md) | `POST /distance-jobs` | [docs](https://www.geocod.io/docs/#distance-jobs-async) |
| [Create Geocoding List](actions/create-geocoding-list.md) | `POST /lists` | [docs](https://www.geocod.io/docs/#create-a-new-list) |
| [Delete Distance Job](actions/delete-distance-job.md) | `DELETE /distance-jobs/{identifier}` | [docs](https://www.geocod.io/docs/#distance-jobs-async) |
| [Delete Geocoding List](actions/delete-geocoding-list.md) | `DELETE /lists/{id}` | [docs](https://www.geocod.io/docs/#delete-a-list) |
| [Download Distance Job Results](actions/download-distance-job-results.md) | `GET /distance-jobs/{identifier}/download` | [docs](https://www.geocod.io/docs/#distance-jobs-async) |
| [Download Geocoding List Results](actions/download-geocoding-list-results.md) | `GET /lists/{id}/download` | [docs](https://www.geocod.io/docs/#download-a-list) |
| [Geocode Address](actions/geocode-address.md) | `GET /geocode` | [docs](https://www.geocod.io/docs/#single-address) |
| [Get Distance Job](actions/get-distance-job.md) | `GET /distance-jobs/{identifier}` | [docs](https://www.geocod.io/docs/#distance-jobs-async) |
| [Get Geocoding List](actions/get-geocoding-list.md) | `GET /lists/{id}` | [docs](https://www.geocod.io/docs/#see-list-status) |
| [List Distance Jobs](actions/list-distance-jobs.md) | `GET /distance-jobs` | [docs](https://www.geocod.io/docs/#distance-jobs-async) |
| [List Geocoding Lists](actions/list-geocoding-lists.md) | `GET /lists` | [docs](https://www.geocod.io/docs/#show-all-lists) |
| [Reverse Geocode Coordinate](actions/reverse-geocode-coordinate.md) | `GET /reverse` | [docs](https://www.geocod.io/docs/#reverse-geocoding-single-coordinate) |
