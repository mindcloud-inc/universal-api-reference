# Get Forecast Along Route with Vaisala Xweather

Retrieves forecast data along a route from Vaisala Xweather API.

## Endpoint

- **Method:** `GET`
- **Path:** `/forecasts/route`
- **Base URL:** `https://data.api.xweather.com`
- **Official documentation:** [Get Forecast Along Route](https://www.xweather.com/docs/weather-api/endpoints/forecasts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `p` | query | `string` | yes | Semicolon-delimited route points using latitude/longitude pairs. |
