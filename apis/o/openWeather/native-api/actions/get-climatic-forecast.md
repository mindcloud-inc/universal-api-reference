# Get Climatic Forecast with OpenWeather

Retrieves a 30-day climate forecast from OpenWeather by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/climate`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Climatic Forecast](https://openweathermap.org/api/forecast30)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
