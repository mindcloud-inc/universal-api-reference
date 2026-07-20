# Golemio API: Native API Reference

A consolidated summary of Golemio API's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://operator-ict.gitlab.io/golemio/documentation/en/open-data-api/
- **OpenAPI specification:** https://api.golemio.cz/docs/static/output-gateway/openapi.json
- **API base URL:** `https://api.golemio.cz`

## Authentication

### API Key

Authenticate with a Golemio API key generated at api.golemio.cz/api-keys. The key is sent to Golemio as the X-Access-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Access-Token: <apiKey>
```

[Official authentication documentation](https://operator-ict.gitlab.io/golemio/documentation/en/open-data-api/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–10000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Air Quality Station History](actions/list-air-quality-station-history.md) | `GET /v2/airqualitystations/history` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Air Quality Stations](actions/list-air-quality-stations.md) | `GET /v2/airqualitystations` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Bicycle Counters](actions/list-bicycle-counters.md) | `GET /v2/bicyclecounters` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List City Districts](actions/list-city-districts.md) | `GET /v2/citydistricts` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Gardens](actions/list-gardens.md) | `GET /v2/gardens` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Medical Institutions](actions/list-medical-institutions.md) | `GET /v2/medicalinstitutions` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Municipal Authorities](actions/list-municipal-authorities.md) | `GET /v2/municipalauthorities` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Municipal Libraries](actions/list-municipal-libraries.md) | `GET /v2/municipallibraries` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Municipal Police Stations](actions/list-municipal-police-stations.md) | `GET /v2/municipalpolicestations` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Parking Locations](actions/list-parking-locations.md) | `GET /v3/parking` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Parking Machines](actions/list-parking-machines.md) | `GET /v3/parking-machines` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Parking Measurements](actions/list-parking-measurements.md) | `GET /v3/parking-measurements` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Parking Sources](actions/list-parking-sources.md) | `GET /v3/parking-sources` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Parking Tariffs](actions/list-parking-tariffs.md) | `GET /v3/parking-tariffs` | [docs](https://api.golemio.cz/docs/public-openapi/) |
| [List Waste Collection Stations](actions/list-waste-collection-stations.md) | `GET /v2/sortedwastestations` | [docs](https://api.golemio.cz/docs/public-openapi/) |
