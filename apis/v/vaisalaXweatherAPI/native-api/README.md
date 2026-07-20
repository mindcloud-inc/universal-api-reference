# Vaisala Xweather: Native API Reference

A consolidated summary of Vaisala Xweather's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.xweather.com/docs/weather-api/
- **API base URL:** `https://data.api.xweather.com`

## Authentication

### Client ID + Client Secret

Use your Xweather client ID and client secret.

### Credentials

- **Client ID:** `clientId` · required · Your Xweather Weather API client ID.
- **Client Secret:** `clientSecret` · required · Your Xweather Weather API client secret.

[Official authentication documentation](https://www.xweather.com/docs/weather-api/getting-started/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Air Quality Index](actions/get-air-quality-index.md) | `GET /airquality/index/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/airquality-index) |
| [Get Air Quality Index Along Route](actions/get-air-quality-index-along-route.md) | `GET /airquality/index/route` | [docs](https://www.xweather.com/docs/weather-api/endpoints/airquality-index) |
| [Get Alert Summaries Within Area](actions/get-alert-summaries-within-area.md) | `GET /alerts/summary/within` | [docs](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary) |
| [Get Alert Summary](actions/get-alert-summary.md) | `GET /alerts/summary/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary) |
| [Get Conditions Along Route](actions/get-conditions-along-route.md) | `GET /conditions/route` | [docs](https://www.xweather.com/docs/weather-api/endpoints/conditions) |
| [Get Conditions Summary](actions/get-conditions-summary.md) | `GET /conditions/summary/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/conditions-summary) |
| [Get Current Conditions](actions/get-current-conditions.md) | `GET /conditions/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/conditions) |
| [Get Current Observations](actions/get-current-observations.md) | `GET /observations/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations) |
| [Get Forecast](actions/get-forecast.md) | `GET /forecasts/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/forecasts) |
| [Get Forecast Along Route](actions/get-forecast-along-route.md) | `GET /forecasts/route` | [docs](https://www.xweather.com/docs/weather-api/endpoints/forecasts) |
| [Get Observation Summary](actions/get-observation-summary.md) | `GET /observations/summary/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations-summary) |
| [Get Observations Along Route](actions/get-observations-along-route.md) | `GET /observations/route` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations) |
| [Get Place](actions/get-place.md) | `GET /places/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/places) |
| [List Alerts](actions/list-alerts.md) | `GET /alerts/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/alerts) |
| [List Archived Observations](actions/list-archived-observations.md) | `GET /observations/archive/:id` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations-archive) |
| [List Archived Observations Within Area](actions/list-archived-observations-within-area.md) | `GET /observations/archive/within` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations-archive) |
| [List Closest Archived Observations](actions/list-closest-archived-observations.md) | `GET /observations/archive/closest` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations-archive) |
| [List Closest Observations](actions/list-closest-observations.md) | `GET /observations/closest` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations) |
| [List Closest Places](actions/list-closest-places.md) | `GET /places/closest` | [docs](https://www.xweather.com/docs/weather-api/endpoints/places) |
| [List Observations Within Area](actions/list-observations-within-area.md) | `GET /observations/within` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations) |
| [List Places Within Area](actions/list-places-within-area.md) | `GET /places/within` | [docs](https://www.xweather.com/docs/weather-api/endpoints/places) |
| [Search Alert Summaries](actions/search-alert-summaries.md) | `GET /alerts/summary/search` | [docs](https://www.xweather.com/docs/weather-api/endpoints/alerts-summary) |
| [Search Observations](actions/search-observations.md) | `GET /observations/search` | [docs](https://www.xweather.com/docs/weather-api/endpoints/observations) |
| [Search Places](actions/search-places.md) | `GET /places/search` | [docs](https://www.xweather.com/docs/weather-api/endpoints/places) |
