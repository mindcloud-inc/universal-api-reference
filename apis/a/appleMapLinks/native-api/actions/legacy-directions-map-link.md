# Legacy Directions Map Link with Apple Map Links

Opens Apple Maps directions using the legacy map link.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Legacy Directions Map Link](https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `daddr` | query | `string` | yes | Legacy directions destination address or coordinate. |
| `saddr` | query | `string` | no | Optional legacy directions starting address or coordinate. |
| `dirflg` | query | `string` | no | Legacy directions mode: d driving, w walking, or r transit. |
