# Get Hourly Forecast with OpenWeather

Retrieves an hourly forecast from OpenWeather by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/2.5/forecast/hourly`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Hourly Forecast](https://openweathermap.org/api/hourly-forecast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
