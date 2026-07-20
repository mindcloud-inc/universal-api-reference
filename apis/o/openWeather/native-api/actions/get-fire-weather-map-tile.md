# Get Fire Weather Map Tile with OpenWeather

Retrieves a fire weather map tile from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://maps.openweathermap.org/maps/2.0/fwi/:z/:x/:y`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Fire Weather Map Tile](https://openweathermap.org/api/fire-index-map)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appid` | query | `string` | yes | OpenWeather API key injected from the app connection. |
| `date` | query | `string` | no | Map date timestamp when required by provider contract. |
| `x` | path | `string` | yes | Tile X coordinate. |
| `y` | path | `string` | yes | Tile Y coordinate. |
| `z` | path | `string` | yes | Tile zoom level. |
