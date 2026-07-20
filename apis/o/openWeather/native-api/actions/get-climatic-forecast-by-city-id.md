# Get Climatic Forecast by City ID with OpenWeather

Retrieves a 30-day climate forecast from OpenWeather by city ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/climate`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Climatic Forecast by City ID](https://openweathermap.org/api/forecast30)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | OpenWeather city identifier. |
