# Get Solar Data with Storm Glass

Retrieves solar data from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/solar/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Solar Data](https://docs.stormglass.io/solar.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired coordinate in decimal degrees. |
| `params` | query | `string` | yes | Comma-separated solar parameters to retrieve, such as uvIndex,solarDownwardRadiationFlux. |
| `source` | query | `string` | no | Optional single source or comma-separated sources. |
| `start` | query | `string` | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | query | `string` | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |
