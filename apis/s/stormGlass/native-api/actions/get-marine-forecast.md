# Get Marine Forecast with Storm Glass

Retrieves marine weather forecasts from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/weather/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Marine Forecast](https://docs.stormglass.io/weather.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired marine coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired marine coordinate in decimal degrees. |
| `params` | query | `string` | yes | Comma-separated marine parameters to retrieve, such as waveHeight,swellHeight,windSpeed. |
| `source` | query | `string` | no | Optional single source or comma-separated sources. Use sg for Storm Glass AI. |
| `start` | query | `string` | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | query | `string` | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |
