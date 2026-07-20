# Get Accumulated Temperature with OpenWeather

Retrieves accumulated temperature data from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://history.openweathermap.org/data/2.5/history/accumulated_temperature`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Accumulated Temperature](https://old.openweathermap.org/api/accumulated-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `start` | query | `number` | yes | Unix timestamp for the start of accumulation. |
| `end` | query | `number` | yes | Unix timestamp for the end of accumulation. |
