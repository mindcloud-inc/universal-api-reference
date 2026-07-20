# Show Place By Address with Apple Map Links

Shows an Apple Maps place card by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/place`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Show Place By Address](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Address string for the place card. |
| `map` | query | `string` | no | Optional map type: explore, driving, transit, satellite, or hybrid. |
