# Calculate Distance Matrix with Geocodio

Retrieves a distance matrix from Geocodio.

## Endpoint

- **Method:** `POST`
- **Path:** `/distance-matrix`
- **Base URL:** `https://api.geocod.io/v1.12`
- **Official documentation:** [Calculate Distance Matrix](https://www.geocod.io/docs/#distance-matrix)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origins[]` | body | `array<string>` | yes | Array of origin coordinates or addresses. |
| `destinations[]` | body | `array<string>` | yes | Array of destination coordinates or addresses. |
| `mode` | body | `string` | no | Distance calculation mode: driving or straightline. Accepted values: `0`, `1`. |
| `units` | body | `string` | no | Distance units: miles or km. Accepted values: `0`, `1`. |
