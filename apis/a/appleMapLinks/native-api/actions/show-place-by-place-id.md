# Show Place By Place ID with Apple Map Links

Shows an Apple Maps place card by Place ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/place`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Show Place By Place ID](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `place-id` | query | `string` | yes | Apple Maps Place ID for the place card. |
| `map` | query | `string` | no | Optional map type: explore, driving, transit, satellite, or hybrid. |
