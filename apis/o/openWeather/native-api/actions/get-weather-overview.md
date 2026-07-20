# Get Weather Overview with OpenWeather

Retrieves an OpenWeather AI weather overview by date.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/3.0/onecall/overview`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Weather Overview](https://openweathermap.org/api/one-call-3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the location. |
| `lon` | query | `number` | yes | Longitude of the location. |
| `date` | query | `string` | yes | Date in YYYY-MM-DD format. |
