# World Health Organization: Native API Reference

A consolidated summary of World Health Organization's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.who.int/data/gho/info/gho-odata-api
- **API base URL:** `https://ghoapi.azureedge.net/api/`

## Authentication

### No authentication

WHO GHO OData endpoints are public and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.who.int/data/gho/info/gho-odata-api)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 1–1000). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Dimension](actions/get-dimension.md) | `GET /DIMENSION/:dimensionCode` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [Get Indicator](actions/get-indicator.md) | `GET /Indicator(':indicatorCode')` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Age Groups](actions/list-age-groups.md) | `GET /DIMENSION/AGEGROUP/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Countries](actions/list-countries.md) | `GET /DIMENSION/COUNTRY/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Dimension Values](actions/list-dimension-values.md) | `GET /DIMENSION/:dimensionCode/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Dimensions](actions/list-dimensions.md) | `GET /Dimension` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Income Groups](actions/list-income-groups.md) | `GET /DIMENSION/WORLDBANKINCOMEGROUP/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Indicator Data](actions/list-indicator-data.md) | `GET /:indicatorCode` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Indicator Dimensions](actions/list-indicator-dimensions.md) | `GET /IndicatorDimension` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Indicators](actions/list-indicators.md) | `GET /Indicator` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List OData Entity Sets](actions/list-odata-entity-sets.md) | `GET /` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Publish States](actions/list-publish-states.md) | `GET /DIMENSION/PUBLISHSTATE/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Region Countries](actions/list-region-countries.md) | `GET /RegionCountry` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Sex Values](actions/list-sex-values.md) | `GET /DIMENSION/SEX/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List WHO Regions](actions/list-who-regions.md) | `GET /DIMENSION/REGION/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
| [List Year Values](actions/list-year-values.md) | `GET /DIMENSION/YEAR/DimensionValues` | [docs](https://www.who.int/data/gho/info/gho-odata-api) |
