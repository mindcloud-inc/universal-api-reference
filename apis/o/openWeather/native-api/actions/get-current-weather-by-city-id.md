# Get Current Weather by City ID with OpenWeather

Retrieves current weather from OpenWeather by city ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/weather`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Current Weather by City ID](https://openweathermap.org/current)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | OpenWeather city identifier. |
