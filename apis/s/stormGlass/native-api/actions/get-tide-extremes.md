# Get Tide Extremes with Storm Glass

Retrieves tide extremes from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/tide/extremes/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Tide Extremes](https://docs.stormglass.io/tide.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired tide coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired tide coordinate in decimal degrees. |
| `start` | query | `string` | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | query | `string` | no | Optional UTC end timestamp as UNIX time or URL-encoded ISO time. |
| `datum` | query | `string` | no | Optional tide datum. Use MSL or MLLW. |
