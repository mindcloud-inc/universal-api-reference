# Get One Call Time Machine with OpenWeather

Retrieves One Call weather from OpenWeather for a timestamp.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/3.0/onecall/timemachine`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get One Call Time Machine](https://openweathermap.org/api/one-call-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `dt` | query | `number` | yes | Unix timestamp for the historical point in time. |
