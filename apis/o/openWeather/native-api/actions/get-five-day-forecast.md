# Get 5 Day Forecast with OpenWeather

Retrieves a 5-day forecast from OpenWeather by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get 5 Day Forecast](https://openweathermap.org/forecast5)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
