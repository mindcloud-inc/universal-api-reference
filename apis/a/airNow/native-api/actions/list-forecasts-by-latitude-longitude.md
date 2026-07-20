# List Forecasts by Latitude Longitude with AirNow

Retrieves air quality forecasts from AirNow by latitude and longitude.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/forecast/latLong/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Forecasts by Latitude Longitude](https://docs.airnowapi.org/ForecastByLatLon/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `latitude` | query | `number` | yes | Latitude for the requested location. |
| `longitude` | query | `number` | yes | Longitude for the requested location. |
| `date` | query | `string` | no | Forecast start date in YYYY-MM-DD format. |
| `distance` | query | `number` | no | Search radius in miles. |
