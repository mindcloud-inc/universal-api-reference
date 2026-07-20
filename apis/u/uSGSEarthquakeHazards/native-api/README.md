# USGS Earthquake Hazards: Native API Reference

A consolidated summary of USGS Earthquake Hazards's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://earthquake.usgs.gov/fdsnws/event/1/
- **API base URL:** `https://earthquake.usgs.gov`

## Authentication

### No authentication

Public USGS Earthquake Hazards endpoints do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://earthquake.usgs.gov/fdsnws/event/1/)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–20000). Use `offset` in the query string as the record offset; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gte`, `lte`.

## Sorting

Set the sort field with `orderby` in the query string. Use `time-asc` for ascending order and `time` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Earthquakes](actions/count-earthquakes.md) | `GET /fdsnws/event/1/count` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [Get All Earthquakes Past Day](actions/get-all-earthquakes-past-day.md) | `GET /earthquakes/feed/v1.0/summary/all_day.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get All Earthquakes Past Hour](actions/get-all-earthquakes-past-hour.md) | `GET /earthquakes/feed/v1.0/summary/all_hour.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get All Earthquakes Past Month](actions/get-all-earthquakes-past-month.md) | `GET /earthquakes/feed/v1.0/summary/all_month.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get All Earthquakes Past Week](actions/get-all-earthquakes-past-week.md) | `GET /earthquakes/feed/v1.0/summary/all_week.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get Earthquake By Event ID](actions/get-earthquake-by-event-id.md) | `GET /fdsnws/event/1/query` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [Get Event API Parameters](actions/get-event-api-parameters.md) | `GET /fdsnws/event/1/application.json` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [Get Event Service Version](actions/get-event-service-version.md) | `GET /fdsnws/event/1/version` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [Get M1.0+ Earthquakes Past Day](actions/get-m10-earthquakes-past-day.md) | `GET /earthquakes/feed/v1.0/summary/1.0_day.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M1.0+ Earthquakes Past Hour](actions/get-m10-earthquakes-past-hour.md) | `GET /earthquakes/feed/v1.0/summary/1.0_hour.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M2.5+ Earthquakes Past Day](actions/get-m25-earthquakes-past-day.md) | `GET /earthquakes/feed/v1.0/summary/2.5_day.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M2.5+ Earthquakes Past Hour](actions/get-m25-earthquakes-past-hour.md) | `GET /earthquakes/feed/v1.0/summary/2.5_hour.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M2.5+ Earthquakes Past Week](actions/get-m25-earthquakes-past-week.md) | `GET /earthquakes/feed/v1.0/summary/2.5_week.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M4.5+ Earthquakes Past Day](actions/get-m45-earthquakes-past-day.md) | `GET /earthquakes/feed/v1.0/summary/4.5_day.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M4.5+ Earthquakes Past Hour](actions/get-m45-earthquakes-past-hour.md) | `GET /earthquakes/feed/v1.0/summary/4.5_hour.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get M4.5+ Earthquakes Past Week](actions/get-m45-earthquakes-past-week.md) | `GET /earthquakes/feed/v1.0/summary/4.5_week.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get Regions For Coordinates](actions/get-regions-for-coordinates.md) | `GET /ws/geoserve/regions.json` | [docs](https://earthquake.usgs.gov/ws/geoserve/regions.php) |
| [Get Significant Earthquakes Past Day](actions/get-significant-earthquakes-past-day.md) | `GET /earthquakes/feed/v1.0/summary/significant_day.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get Significant Earthquakes Past Hour](actions/get-significant-earthquakes-past-hour.md) | `GET /earthquakes/feed/v1.0/summary/significant_hour.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get Significant Earthquakes Past Month](actions/get-significant-earthquakes-past-month.md) | `GET /earthquakes/feed/v1.0/summary/significant_month.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [Get Significant Earthquakes Past Week](actions/get-significant-earthquakes-past-week.md) | `GET /earthquakes/feed/v1.0/summary/significant_week.geojson` | [docs](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) |
| [List Earthquake Catalogs](actions/list-earthquake-catalogs.md) | `GET /fdsnws/event/1/catalogs` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [List Earthquake Contributors](actions/list-earthquake-contributors.md) | `GET /fdsnws/event/1/contributors` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
| [Search Earthquakes](actions/search-earthquakes.md) | `GET /fdsnws/event/1/query` | [docs](https://earthquake.usgs.gov/fdsnws/event/1/) |
