# Get One Call Weather with OpenWeather

Retrieves One Call weather data from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/3.0/onecall`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get One Call Weather](https://openweathermap.org/api/one-call-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
