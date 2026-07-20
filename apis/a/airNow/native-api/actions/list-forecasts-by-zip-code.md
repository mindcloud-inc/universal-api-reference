# List Forecasts by Zip Code with AirNow

Retrieves air quality forecasts from AirNow by zip code.

## Endpoint

- **Method:** `GET`
- **Path:** `/aq/forecast/zipCode/`
- **Base URL:** `https://www.airnowapi.org`
- **Official documentation:** [List Forecasts by Zip Code](https://docs.airnowapi.org/ForecastByZip/query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zipCode` | query | `string` | yes | The zip code used to resolve the reporting area. |
| `date` | query | `string` | no | Forecast start date in YYYY-MM-DD format. |
| `distance` | query | `number` | no | Search radius in miles. |
