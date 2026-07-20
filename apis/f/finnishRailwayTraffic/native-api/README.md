# Finnish Railway Traffic: Native API Reference

A consolidated summary of Finnish Railway Traffic's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.digitraffic.fi/en/railway-traffic/
- **OpenAPI specification:** https://rata.digitraffic.fi/swagger/openapi.json
- **API base URL:** `https://rata.digitraffic.fi`

## Authentication

### No authentication

Digitraffic railway APIs are public open data and do not require API keys, OAuth, or account credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.digitraffic.fi/en/support/instructions/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get latest train by number](actions/get-latest-train-by-number.md) | `GET /api/v1/trains/latest/:train_number` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List active passenger information messages](actions/list-active-passenger-information-messages.md) | `GET /api/v1/passenger-information/active` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List cause category codes](actions/list-cause-category-codes.md) | `GET /api/v1/metadata/cause-category-codes` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List compositions by departure date](actions/list-compositions-by-departure-date.md) | `GET /api/v1/compositions/:departure_date` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List compositions updated after version](actions/list-compositions-updated-after-version.md) | `GET /api/v1/compositions` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List detailed cause category codes](actions/list-detailed-cause-category-codes.md) | `GET /api/v1/metadata/detailed-cause-category-codes` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List latest train locations](actions/list-latest-train-locations.md) | `GET /api/v1/train-locations/latest` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List latest train locations as GeoJSON](actions/list-latest-train-locations-as-geojson.md) | `GET /api/v1/train-locations.geojson/latest` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List live trains](actions/list-live-trains.md) | `GET /api/v1/live-trains` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List live trains by station](actions/list-live-trains-by-station.md) | `GET /api/v1/live-trains/station/:station` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List operators](actions/list-operators.md) | `GET /api/v1/metadata/operators` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List passenger information messages updated after date](actions/list-passenger-information-messages-updated-after-date.md) | `GET /api/v1/passenger-information/updated-after/:date` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List routesets updated after version](actions/list-routesets-updated-after-version.md) | `GET /api/v1/routesets` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List stations](actions/list-stations.md) | `GET /api/v1/metadata/stations` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List stations as GeoJSON](actions/list-stations-as-geojson.md) | `GET /api/v1/metadata/stations.geojson` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List third cause category codes](actions/list-third-cause-category-codes.md) | `GET /api/v1/metadata/third-cause-category-codes` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List timetable periods](actions/list-timetable-periods.md) | `GET /api/v1/metadata/time-table-periods` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List track sections](actions/list-track-sections.md) | `GET /api/v1/metadata/track-sections` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List trackwork notification status](actions/list-trackwork-notification-status.md) | `GET /api/v1/trackwork-notifications/status` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List trackwork notifications](actions/list-trackwork-notifications.md) | `GET /api/v1/trackwork-notifications.json` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List trackwork notifications as GeoJSON](actions/list-trackwork-notifications-as-geojson.md) | `GET /api/v1/trackwork-notifications.geojson` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List traffic restriction notification status](actions/list-traffic-restriction-notification-status.md) | `GET /api/v1/trafficrestriction-notifications/status` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List traffic restriction notifications](actions/list-traffic-restriction-notifications.md) | `GET /api/v1/trafficrestriction-notifications.json` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List traffic restriction notifications as GeoJSON](actions/list-traffic-restriction-notifications-as-geojson.md) | `GET /api/v1/trafficrestriction-notifications.geojson` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List train categories](actions/list-train-categories.md) | `GET /api/v1/metadata/train-categories` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List train running message rules](actions/list-train-running-message-rules.md) | `GET /api/v1/metadata/train-running-message-rules` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List train tracking messages updated after version](actions/list-train-tracking-messages-updated-after-version.md) | `GET /api/v1/train-tracking/` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List train types](actions/list-train-types.md) | `GET /api/v1/metadata/train-types` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List trains by departure date](actions/list-trains-by-departure-date.md) | `GET /api/v1/trains/:departure_date` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [List trains updated after version](actions/list-trains-updated-after-version.md) | `GET /api/v1/trains` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
| [Search live trains between stations](actions/search-live-trains-between-stations.md) | `GET /api/v1/live-trains/station/:departure_station/:arrival_station` | [docs](https://rata.digitraffic.fi/swagger/openapi.json) |
