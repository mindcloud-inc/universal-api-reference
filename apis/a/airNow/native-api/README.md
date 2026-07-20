# AirNow: Native API Reference

A consolidated summary of AirNow's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.airnowapi.org/webservices
- **API base URL:** `https://www.airnowapi.org`

## Authentication

### API Key

Use an AirNow API key. AirNow web services require the tenant API key as the API_KEY query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Your AirNow API key from the Web Services page.

[Official authentication documentation](https://docs.airnowapi.org/Data/)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Current Observations by Latitude Longitude](actions/list-current-observations-by-latitude-longitude.md) | `GET /aq/observation/latLong/current/` | [docs](https://docs.airnowapi.org/CurrentObservationsByLatLon/query) |
| [List Current Observations by Zip Code](actions/list-current-observations-by-zip-code.md) | `GET /aq/observation/zipCode/current/` | [docs](https://docs.airnowapi.org/CurrentObservationsByZip/query) |
| [List Forecasts by Latitude Longitude](actions/list-forecasts-by-latitude-longitude.md) | `GET /aq/forecast/latLong/` | [docs](https://docs.airnowapi.org/ForecastByLatLon/query) |
| [List Forecasts by Zip Code](actions/list-forecasts-by-zip-code.md) | `GET /aq/forecast/zipCode/` | [docs](https://docs.airnowapi.org/ForecastByZip/query) |
| [List Historical Observations by Latitude Longitude](actions/list-historical-observations-by-latitude-longitude.md) | `GET /aq/observation/latLong/historical/` | [docs](https://docs.airnowapi.org/HistoricalObservationsByLatLong/query) |
| [List Historical Observations by Zip Code](actions/list-historical-observations-by-zip-code.md) | `GET /aq/observation/zipCode/historical/` | [docs](https://docs.airnowapi.org/HistoricalObservationsByZip/query) |
| [List Monitoring Site Observations](actions/list-monitoring-site-observations.md) | `GET /aq/data/` | [docs](https://docs.airnowapi.org/ObservationsByMonitoringSite/query) |
