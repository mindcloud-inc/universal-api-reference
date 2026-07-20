# Get Bio Data with Storm Glass

Retrieves bio data from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/bio/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Bio Data](https://docs.stormglass.io/bio.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired coordinate in decimal degrees. |
| `params` | query | `string` | yes | Comma-separated bio parameters to retrieve, such as soilMoisture,soilTemperature,salinity. |
| `source` | query | `string` | no | Optional single source or comma-separated sources. |
| `start` | query | `string` | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | query | `string` | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |
