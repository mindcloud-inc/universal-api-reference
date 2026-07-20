# Get Daily Forecast by City ID with OpenWeather

Retrieves a daily forecast from OpenWeather by city ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/daily`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Daily Forecast by City ID](https://openweathermap.org/forecast16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | OpenWeather city identifier. |
