# Ambee: Native API Reference

A consolidated summary of Ambee's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.ambeedata.com/apis/overview
- **API base URL:** `https://api.ambeedata.com`

## Authentication

### API Key

Authenticate Ambee requests with your Ambee API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.ambeedata.com/apis/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Geocode By Place](actions/geocode-by-place.md) | `GET /geocode/by-place` | [docs](https://docs.ambeedata.com/apis/location#geocoding-placewise) |
| [Get Air Quality Forecast By Coordinates](actions/get-air-quality-forecast-by-coordinates.md) | `GET /forecast/aq/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/air-quality#forecast-geospatial) |
| [Get Latest Air Quality By City](actions/get-latest-air-quality-by-city.md) | `GET /latest/by-city` | [docs](https://docs.ambeedata.com/apis/air-quality#latest-citywise) |
| [Get Latest Air Quality By Coordinates](actions/get-latest-air-quality-by-coordinates.md) | `GET /latest/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/air-quality#latest-geospatial) |
| [Get Latest Air Quality By Country Code](actions/get-latest-air-quality-by-country-code.md) | `GET /latest/by-country-code` | [docs](https://docs.ambeedata.com/apis/air-quality#latest-countrywise) |
| [Get Latest Air Quality By Postal Code](actions/get-latest-air-quality-by-postal-code.md) | `GET /latest/by-postal-code` | [docs](https://docs.ambeedata.com/apis/air-quality#latest-postalcode) |
| [Get Latest Wildfire By Coordinates](actions/get-latest-wildfire-by-coordinates.md) | `GET /fire/latest/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/fire#latest-geospatial) |
| [Get Wildfire Forecast By Coordinates](actions/get-wildfire-forecast-by-coordinates.md) | `GET /fire/risk/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/fire#forecast-geospatial) |
| [Retrieve Latest Pollen By Coordinates](actions/retrieve-latest-pollen-by-coordinates.md) | `GET /latest/pollen/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/pollen#latest-geospatial) |
| [Retrieve Latest Pollen By Place](actions/retrieve-latest-pollen-by-place.md) | `GET /latest/pollen/by-place` | [docs](https://docs.ambeedata.com/apis/pollen#latest-placewise) |
| [Retrieve Latest Weather By Coordinates](actions/retrieve-latest-weather-by-coordinates.md) | `GET /weather/latest/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/weather#latest-geospatial) |
| [Retrieve Latest Wildfire By Place](actions/retrieve-latest-wildfire-by-place.md) | `GET /fire/latest/by-place` | [docs](https://docs.ambeedata.com/apis/fire#latest-placewise) |
| [Retrieve Pollen Forecast By Coordinates](actions/retrieve-pollen-forecast-by-coordinates.md) | `GET /forecast/pollen/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/pollen#forecast-geospatial) |
| [Retrieve Pollen Forecast By Place](actions/retrieve-pollen-forecast-by-place.md) | `GET /forecast/pollen/by-place` | [docs](https://docs.ambeedata.com/apis/pollen#forecast-placewise) |
| [Retrieve Pollen 120hr Forecast By Coordinates](actions/retrieve-pollen120hr-forecast-by-coordinates.md) | `GET /forecast/v2/pollen/120hr/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/pollen#forecast-geospatial-120hr) |
| [Retrieve Pollen 120hr Forecast By Place](actions/retrieve-pollen120hr-forecast-by-place.md) | `GET /forecast/v2/pollen/120hr/by-place` | [docs](https://docs.ambeedata.com/apis/pollen#forecast-placewise-120hr) |
| [Retrieve Weather Forecast By Coordinates](actions/retrieve-weather-forecast-by-coordinates.md) | `GET /weather/forecast/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/weather#forecast-geospatial) |
| [Retrieve Wildfire Forecast By Place](actions/retrieve-wildfire-forecast-by-place.md) | `GET /fire/risk/by-place` | [docs](https://docs.ambeedata.com/apis/fire#forecast-placewise) |
| [Reverse Geocode By Coordinates](actions/reverse-geocode-by-coordinates.md) | `GET /geocode/reverse/by-lat-lng` | [docs](https://docs.ambeedata.com/apis/location#reverse-geocoding-geospatial) |
