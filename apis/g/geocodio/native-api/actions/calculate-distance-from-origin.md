# Calculate Distance From Origin with Geocodio

Retrieves distances from one origin in Geocodio.

## Endpoint

- **Method:** `GET`
- **Path:** `/distance`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Calculate Distance From Origin](https://www.geocod.io/docs/#single-origin-distance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origin` | query | `string` | yes | Origin coordinate or address. |
| `destinations[]` | query | `array<string>` | yes | Destination coordinates or addresses. |
| `mode` | query | `string` | no | Distance calculation mode: driving or straightline. Accepted values: `0`, `1`. |
| `units` | query | `string` | no | Distance units: miles or km. Accepted values: `0`, `1`. |
