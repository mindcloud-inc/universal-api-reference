# Get One Call Daily Summary with OpenWeather

Retrieves a One Call daily summary from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/3.0/onecall/day_summary`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get One Call Daily Summary](https://openweathermap.org/api/one-call-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `date` | query | `string` | yes | Date in YYYY-MM-DD format. |
