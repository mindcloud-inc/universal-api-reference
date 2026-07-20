# EONET: Native API Reference

A consolidated summary of EONET's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://eonet.gsfc.nasa.gov/docs/v3
- **API base URL:** `https://eonet.gsfc.nasa.gov/api/v3`

## Authentication

### No Authentication

Public EONET API access without credentials.

This API does not require request authentication.

[Official authentication documentation](https://eonet.gsfc.nasa.gov/docs/v3)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20).

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | `GET /events/:eventId` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events-api) |
| [List Atom Event Feed Items](actions/list-atom-event-feed-items.md) | `GET /events/atom` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events-api) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#categories-api) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events) |
| [List Events for Category](actions/list-events-for-category.md) | `GET /categories/:categoryId` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#categories-api) |
| [List GeoJSON Event Features](actions/list-geojson-event-features.md) | `GET /events/geojson` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events-api-geojson) |
| [List GeoJSON Event Features for Event](actions/list-geojson-event-features-for-event.md) | `GET /events/:eventId/geojson` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events-api-geojson) |
| [List Layers](actions/list-layers.md) | `GET /layers` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#layers-api) |
| [List Layers for Category](actions/list-layers-for-category.md) | `GET /layers/:categoryId` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#layers-api) |
| [List Magnitudes](actions/list-magnitudes.md) | `GET /magnitudes` | [docs](https://eonet.gsfc.nasa.gov/docs/v3) |
| [List RSS Event Feed Items](actions/list-rss-event-feed-items.md) | `GET /events/rss` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#events-api) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://eonet.gsfc.nasa.gov/docs/v3#sources-fields) |
