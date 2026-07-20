# Show Place By Coordinate with Apple Map Links

Shows an Apple Maps place card by coordinate.

## Endpoint

- **Method:** `GET`
- **Path:** `/place`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Show Place By Coordinate](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinate` | query | `string` | yes | Place location as a comma-separated latitude,longitude coordinate pair. |
| `name` | query | `string` | no | Optional custom name to display on the place card. |
| `map` | query | `string` | no | Optional map type: explore, driving, transit, satellite, or hybrid. |
