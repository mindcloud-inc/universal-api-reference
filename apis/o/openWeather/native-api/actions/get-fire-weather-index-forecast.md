# Get Fire Weather Index Forecast with OpenWeather

Retrieves a fire weather index forecast from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.openweathermap.org/data/2.5/fwi/forecast`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Fire Weather Index Forecast](https://openweathermap.org/api/fire-index-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `string` | yes | Latitude of the location. |
| `lon` | query | `string` | yes | Longitude of the location. |
