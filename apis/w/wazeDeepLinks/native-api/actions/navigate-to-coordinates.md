# Navigate To Coordinates with Waze Deep Links

Generates a Waze navigation URL for map coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `https://waze.com/ul`
- **Base URL:** `https://waze.com/ul`
- **Official documentation:** [Navigate To Coordinates](https://developers.google.com/waze/deeplinks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ll` | query | `string` | yes | Latitude and longitude as lat,lng. |
| `z` | query | `number` | no | Map magnification level from 6 to 8192. |
