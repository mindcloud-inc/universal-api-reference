# IQAir AirVisual: Native API Reference

A consolidated summary of IQAir AirVisual's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.iqair.com/
- **API base URL:** `https://api.airvisual.com`

## Authentication

### API Key

Use an IQAir AirVisual API key. The AirVisual API requires the tenant key as the shared `key` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Your IQAir AirVisual Community API key.

[Official authentication documentation](https://api-docs.iqair.com/)

## API conventions

Response data is read from `data`.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get City Air Quality](actions/get-city-air-quality.md) | `GET /v2/city` | [docs](https://api-docs.iqair.com/) |
| [Get City Ranking](actions/get-city-ranking.md) | `GET /v2/city_ranking` | [docs](https://api-docs.iqair.com/) |
| [Get Nearest City Air Quality](actions/get-nearest-city-air-quality.md) | `GET /v2/nearest_city` | [docs](https://api-docs.iqair.com/) |
| [Get Nearest City Air Quality By IP](actions/get-nearest-city-air-quality-by-ip.md) | `GET /v2/nearest_city` | [docs](https://api-docs.iqair.com/) |
| [Get Nearest Station Air Quality](actions/get-nearest-station-air-quality.md) | `GET /v2/nearest_station` | [docs](https://api-docs.iqair.com/) |
| [Get Nearest Station Air Quality By IP](actions/get-nearest-station-air-quality-by-ip.md) | `GET /v2/nearest_station` | [docs](https://api-docs.iqair.com/) |
| [Get Station Air Quality](actions/get-station-air-quality.md) | `GET /v2/station` | [docs](https://api-docs.iqair.com/) |
| [List Cities](actions/list-cities.md) | `GET /v2/cities` | [docs](https://api-docs.iqair.com/) |
| [List Countries](actions/list-countries.md) | `GET /v2/countries` | [docs](https://api-docs.iqair.com/) |
| [List States](actions/list-states.md) | `GET /v2/states` | [docs](https://api-docs.iqair.com/) |
| [List Stations](actions/list-stations.md) | `GET /v2/stations` | [docs](https://api-docs.iqair.com/) |
