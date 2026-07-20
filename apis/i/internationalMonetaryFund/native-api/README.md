# International Monetary Fund: Native API Reference

A consolidated summary of International Monetary Fund's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://www.imf.org/external/datamapper/api/
- **API base URL:** `https://www.imf.org/external/datamapper/api/v1`

## Authentication

### No Authentication

Public IMF DataMapper API access requires no login, API key, or OAuth setup.

This API does not require request authentication.

[Official authentication documentation](https://www.imf.org/external/datamapper/api/)

## API conventions

Responses from this API use plain text.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Indicator Time Series](actions/get-indicator-time-series.md) | `GET /:indicatorId` | [docs](https://www.imf.org/external/datamapper/api/) |
| [Get Scoped Time Series](actions/get-scoped-time-series.md) | `GET /:indicatorId/:selectionPath` | [docs](https://www.imf.org/external/datamapper/api/) |
| [List Analytical Groups](actions/list-analytical-groups.md) | `GET /groups` | [docs](https://www.imf.org/external/datamapper/api/) |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://www.imf.org/external/datamapper/api/) |
| [List Indicators](actions/list-indicators.md) | `GET /indicators` | [docs](https://www.imf.org/external/datamapper/api/) |
| [List Regions](actions/list-regions.md) | `GET /regions` | [docs](https://www.imf.org/external/datamapper/api/) |
