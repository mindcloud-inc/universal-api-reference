# Get Hourly Forecast by City ID with OpenWeather

Retrieves an hourly forecast from OpenWeather by city ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/hourly`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Hourly Forecast by City ID](https://openweathermap.org/api/hourly-forecast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | OpenWeather city identifier. |
