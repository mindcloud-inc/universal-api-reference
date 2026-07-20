# Frame Map with Apple Map Links

Frames a map view in Apple Maps.

## Endpoint

- **Method:** `GET`
- **Path:** `/frame`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Frame Map](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `center` | query | `string` | yes | Map center as a comma-separated latitude,longitude coordinate pair. |
| `span` | query | `string` | no | Visible area span around the center as latitudeDelta,longitudeDelta. |
| `map` | query | `string` | no | Map type: explore, driving, transit, satellite, or hybrid. |
| `mode` | query | `string` | no | Optional location tracking mode: follow, follow-with-heading, or none. |
| `heading` | query | `number` | no | Map camera heading in degrees. |
| `pitch` | query | `number` | no | Map camera pitch angle. |
| `distance` | query | `number` | no | Apparent distance from the viewer to the map surface. |
