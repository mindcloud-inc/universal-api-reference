# Get Daily Forecast with OpenWeather

Retrieves a daily forecast from OpenWeather by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/daily`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Daily Forecast](https://openweathermap.org/forecast16)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
