# Get Historical Weather with OpenWeather

Retrieves historical weather data from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://history.openweathermap.org/data/2.5/history/city`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Historical Weather](https://old.openweathermap.org/history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `type` | query | `string` | yes | Provider history query type. |
| `start` | query | `number` | yes | Unix timestamp for the start of the requested history window. |
| `end` | query | `number` | yes | Unix timestamp for the end of the requested history window. |
