# NCEI Climate Data: Native API Reference

A consolidated summary of NCEI Climate Data's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://www.ncei.noaa.gov/cdo-web/webservices/v2
- **API base URL:** `https://www.ncei.noaa.gov/cdo-web/api/v2`

## Authentication

### API Key

Use an NCEI Climate Data Online API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://www.ncei.noaa.gov/cdo-web/webservices/v2)

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Data Category](actions/get-data-category.md) | `GET /datacategories/[:dataCategoryId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-categories) |
| [Get Data Type](actions/get-data-type.md) | `GET /datatypes/[:dataTypeId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-types) |
| [Get Dataset](actions/get-dataset.md) | `GET /datasets/[:datasetId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#datasets) |
| [Get Location](actions/get-location.md) | `GET /locations/[:locationId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#locations) |
| [Get Location Category](actions/get-location-category.md) | `GET /locationcategories/[:locationCategoryId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#location-categories) |
| [Get Station](actions/get-station.md) | `GET /stations/[:stationId]` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#stations) |
| [List Climate Data](actions/list-climate-data.md) | `GET /data` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data) |
| [List Data Categories](actions/list-data-categories.md) | `GET /datacategories` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-categories) |
| [List Data Types](actions/list-data-types.md) | `GET /datatypes` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#data-types) |
| [List Datasets](actions/list-datasets.md) | `GET /datasets` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#datasets) |
| [List Location Categories](actions/list-location-categories.md) | `GET /locationcategories` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#location-categories) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#locations) |
| [List Stations](actions/list-stations.md) | `GET /stations` | [docs](https://www.ncei.noaa.gov/cdo-web/webservices/v2#stations) |
