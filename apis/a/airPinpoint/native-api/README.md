# AirPinpoint: Native API Reference

A consolidated summary of AirPinpoint's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://airpinpoint.com/docs/api
- **API base URL:** `https://api.airpinpoint.com/v1`

## Authentication

### API Key

Use an AirPinpoint dashboard API key. The platform sends it as Authorization: Bearer <apiKey>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://airpinpoint.com/docs/api)

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Geofence](actions/create-geofence.md) | `POST /geofences` | [docs](https://airpinpoint.com/docs/geofences) |
| [Delete Geofence](actions/delete-geofence.md) | `DELETE /geofences/{geofence_id}` | [docs](https://airpinpoint.com/docs/geofences) |
| [Generate Share Link](actions/generate-share-link.md) | `POST /share-links` | [docs](https://airpinpoint.com/docs/share-links) |
| [Get Trackable](actions/get-trackable.md) | `GET /trackables/{trackableId}` | [docs](https://airpinpoint.com/docs/trackables) |
| [Get Trackable Battery](actions/get-trackable-battery.md) | `GET /trackables/{trackableId}/battery` | [docs](https://airpinpoint.com/docs/trackables) |
| [Get Trackable Locations](actions/get-trackable-locations.md) | `GET /trackables/{trackableId}/locations` | [docs](https://airpinpoint.com/docs/locations) |
| [List Geofences](actions/list-geofences.md) | `GET /geofences` | [docs](https://airpinpoint.com/docs/geofences) |
| [List Trackables](actions/list-trackables.md) | `GET /trackables` | [docs](https://airpinpoint.com/docs/trackables) |
| [Reset Trackable Battery](actions/reset-trackable-battery.md) | `POST /trackables/{trackableId}/battery` | [docs](https://airpinpoint.com/docs/trackables) |
| [Test Geofence Webhook](actions/test-geofence-webhook.md) | `POST /geofences/{geofence_id}/test-webhook` | [docs](https://airpinpoint.com/docs/webhooks) |
| [Update Geofence](actions/update-geofence.md) | `PATCH /geofences/{geofence_id}` | [docs](https://airpinpoint.com/docs/geofences) |
