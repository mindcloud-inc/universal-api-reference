# Get Weather Map Tile with OpenWeather

Retrieves a weather map tile from OpenWeather.

## Endpoint

- **Method:** `GET`
- **Path:** `https://tile.openweathermap.org/map/:layer/:z/:x/:y.png`
- **Base URL:** `https://api.openweathermap.org`
- **Official documentation:** [Get Weather Map Tile](https://openweathermap.org/api/weathermaps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appid` | query | `string` | yes | OpenWeather API key injected from the app connection. |
| `layer` | path | `string` | yes | Map layer code. |
| `x` | path | `string` | yes | Tile X coordinate. |
| `y` | path | `string` | yes | Tile Y coordinate. |
| `z` | path | `string` | yes | Tile zoom level. |
