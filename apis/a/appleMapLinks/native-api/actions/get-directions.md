# Get Directions with Apple Map Links

Opens Apple Maps directions between locations.

## Endpoint

- **Method:** `GET`
- **Path:** `/directions`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Get Directions](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `string` | no | Optional starting point as an address, coordinate, or place name. |
| `source-place-id` | query | `string` | no | Optional Place ID for the source; requires source. |
| `destination` | query | `string` | yes | Ending destination as an address, coordinate, or place name. |
| `destination-place-id` | query | `string` | no | Optional Place ID for the destination; requires destination. |
| `waypoint` | query | `string` | no | Optional intermediate stop. Apple Maps allows repeating this query parameter for multistop routing. |
| `waypoint-place-id` | query | `string` | no | Optional Place ID for a waypoint. |
| `mode` | query | `string` | no | Transportation mode: driving, walking, transit, or cycling. |
| `avoid` | query | `string` | no | Comma-delimited route avoid preferences, such as tolls, highways, busy-roads, or stairs. |
| `transit-preferences` | query | `string` | no | Comma-delimited transit preferences: bus, subway, commuter, or ferry. |
| `start` | query | `number` | no | Delay in seconds before starting navigation. |
