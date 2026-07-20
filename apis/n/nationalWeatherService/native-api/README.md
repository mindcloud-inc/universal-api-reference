# National Weather Service: Native API Reference

A consolidated summary of National Weather Service's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.weather.gov/documentation/services-web-api
- **OpenAPI specification:** https://api.weather.gov/openapi.json
- **API base URL:** `https://api.weather.gov`

## Authentication

### Public API

Uses the public National Weather Service API. Requests must include a unique User-Agent header; no secret credentials are required.

This API does not require request authentication.

[Official authentication documentation](https://www.weather.gov/documentation/services-web-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud Gravity App Builder (support@mindcloud.co)` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 500; accepted range 1–500). Use `cursor` in the query string as the pagination cursor; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Active Alerts](actions/count-active-alerts.md) | `GET /alerts/active/count` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1count/get) |
| [Get Alert](actions/get-alert.md) | `GET /alerts/:id` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1{id}/get) |
| [Get Forecast Office](actions/get-forecast-office.md) | `GET /offices/:officeId` | [docs](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}/get) |
| [Get Gridpoint Forecast](actions/get-gridpoint-forecast.md) | `GET /gridpoints/:wfo/:x,:y/forecast` | [docs](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}~1forecast/get) |
| [Get Gridpoint Hourly Forecast](actions/get-gridpoint-hourly-forecast.md) | `GET /gridpoints/:wfo/:x,:y/forecast/hourly` | [docs](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}~1forecast~1hourly/get) |
| [Get Gridpoint Raw Forecast Data](actions/get-gridpoint-raw-forecast-data.md) | `GET /gridpoints/:wfo/:x,:y` | [docs](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}/get) |
| [Get Latest Product By Type And Location](actions/get-latest-product-by-type-and-location.md) | `GET /products/types/:typeId/locations/:locationId/latest` | [docs](https://api.weather.gov/openapi.json#/paths/~1products~1types~1{typeId}~1locations~1{locationId}~1latest/get) |
| [Get Latest Station Observation](actions/get-latest-station-observation.md) | `GET /stations/:stationId/observations/latest` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations~1latest/get) |
| [Get Observation Station](actions/get-observation-station.md) | `GET /stations/:stationId` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}/get) |
| [Get Office Briefing](actions/get-office-briefing.md) | `GET /offices/:officeId/briefing` | [docs](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1briefing/get) |
| [Get Office Headline](actions/get-office-headline.md) | `GET /offices/:officeId/headlines/:headlineId` | [docs](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1headlines~1{headlineId}/get) |
| [Get Office Weather Stories](actions/get-office-weather-stories.md) | `GET /offices/:officeId/weatherstories` | [docs](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1weatherstories/get) |
| [Get Point Weather Radio Script](actions/get-point-weather-radio-script.md) | `GET /points/:latitude,:longitude/radio` | [docs](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}~1radio/get) |
| [Get Station Observation By Time](actions/get-station-observation-by-time.md) | `GET /stations/:stationId/observations/:time` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations~1{time}/get) |
| [Get Text Product](actions/get-text-product.md) | `GET /products/:productId` | [docs](https://api.weather.gov/openapi.json#/paths/~1products~1{productId}/get) |
| [Get Zone](actions/get-zone.md) | `GET /zones/:type/:zoneId` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}~1{zoneId}/get) |
| [Get Zone Forecast](actions/get-zone-forecast.md) | `GET /zones/:type/:zoneId/forecast` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}~1{zoneId}~1forecast/get) |
| [List Active Alerts](actions/list-active-alerts.md) | `GET /alerts/active` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1active/get) |
| [List Active Alerts By Area](actions/list-active-alerts-by-area.md) | `GET /alerts/active/area/:area` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1area~1{area}/get) |
| [List Active Alerts By Marine Region](actions/list-active-alerts-by-marine-region.md) | `GET /alerts/active/region/:region` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1region~1{region}/get) |
| [List Active Alerts By Zone](actions/list-active-alerts-by-zone.md) | `GET /alerts/active/zone/:zoneId` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts~1active~1zone~1{zoneId}/get) |
| [List Alert Types](actions/list-alert-types.md) | `GET /alerts/types` | [docs](https://api.weather.gov/openapi.json) |
| [List Center Weather Advisories](actions/list-center-weather-advisories.md) | `GET /aviation/cwsus/:cwsuId/cwas` | [docs](https://api.weather.gov/openapi.json#/paths/~1aviation~1cwsus~1{cwsuId}~1cwas/get) |
| [List Gridpoint Observation Stations](actions/list-gridpoint-observation-stations.md) | `GET /gridpoints/:wfo/:x,:y/stations` | [docs](https://api.weather.gov/openapi.json#/paths/~1gridpoints~1{wfo}~1{x},{y}~1stations/get) |
| [List Observation Stations](actions/list-observation-stations.md) | `GET /stations` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations/get) |
| [List Office Headlines](actions/list-office-headlines.md) | `GET /offices/:officeId/headlines` | [docs](https://api.weather.gov/openapi.json#/paths/~1offices~1{officeId}~1headlines/get) |
| [List Point Observation Stations](actions/list-point-observation-stations.md) | `GET /points/:latitude,:longitude/stations` | [docs](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}~1stations/get) |
| [List Products By Type](actions/list-products-by-type.md) | `GET /products/types/:typeId` | [docs](https://api.weather.gov/openapi.json#/paths/~1products~1types~1{typeId}/get) |
| [List SIGMETs And AIRMETs](actions/list-sigmets-and-airmets.md) | `GET /aviation/sigmets` | [docs](https://api.weather.gov/openapi.json#/paths/~1aviation~1sigmets/get) |
| [List Station Observations](actions/list-station-observations.md) | `GET /stations/:stationId/observations` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1observations/get) |
| [List Station TAFs](actions/list-station-tafs.md) | `GET /stations/:stationId/tafs` | [docs](https://api.weather.gov/openapi.json#/paths/~1stations~1{stationId}~1tafs/get) |
| [List Text Product Locations](actions/list-text-product-locations.md) | `GET /products/locations` | [docs](https://api.weather.gov/openapi.json#/paths/~1products~1locations/get) |
| [List Text Product Types](actions/list-text-product-types.md) | `GET /products/types` | [docs](https://api.weather.gov/openapi.json#/paths/~1products~1types/get) |
| [List Zone Forecast Observations](actions/list-zone-forecast-observations.md) | `GET /zones/forecast/:zoneId/observations` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones~1forecast~1{zoneId}~1observations/get) |
| [List Zone Observation Stations](actions/list-zone-observation-stations.md) | `GET /zones/forecast/:zoneId/stations` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones~1forecast~1{zoneId}~1stations/get) |
| [List Zones](actions/list-zones.md) | `GET /zones` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones/get) |
| [List Zones By Type](actions/list-zones-by-type.md) | `GET /zones/:type` | [docs](https://api.weather.gov/openapi.json#/paths/~1zones~1{type}/get) |
| [Query Alerts](actions/query-alerts.md) | `GET /alerts` | [docs](https://api.weather.gov/openapi.json#/paths/~1alerts/get) |
| [Resolve Point Metadata](actions/resolve-point-metadata.md) | `GET /points/:latitude,:longitude` | [docs](https://api.weather.gov/openapi.json#/paths/~1points~1{latitude},{longitude}/get) |
| [Search Text Products](actions/search-text-products.md) | `GET /products` | [docs](https://api.weather.gov/openapi.json#/paths/~1products/get) |
