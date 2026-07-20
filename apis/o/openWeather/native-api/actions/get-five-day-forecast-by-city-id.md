# Get 5 Day Forecast by City ID with OpenWeather

Retrieves a 5-day forecast from OpenWeather by city ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get 5 Day Forecast by City ID](https://openweathermap.org/forecast5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | OpenWeather city identifier. |
