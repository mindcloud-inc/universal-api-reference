# Get Astronomy with Storm Glass

Retrieves astronomy data from Storm Glass.

## Endpoint

- **Method:** `GET`
- **Path:** `/astronomy/point`
- **Base URL:** `https://api.stormglass.io/v2`
- **Official documentation:** [Get Astronomy](https://docs.stormglass.io/astronomy.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Latitude of the desired coordinate in decimal degrees. |
| `lng` | query | `number` | yes | Longitude of the desired coordinate in decimal degrees. |
| `start` | query | `string` | no | Optional UTC start timestamp as UNIX time or URL-encoded ISO time. |
| `end` | query | `string` | no | Optional UTC end date or timestamp. Storm Glass returns astronomy data for up to 10 days. |
