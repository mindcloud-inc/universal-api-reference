# Get Forecast with Vaisala Xweather

Retrieves forecast data from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/:id`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Forecast](https://www.xweather.com/docs/weather-api/endpoints/forecasts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location, place identifier, or latitude/longitude. |
