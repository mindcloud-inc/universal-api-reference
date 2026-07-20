# Legacy Coordinate Map Link with Apple Map Links

Shows an Apple Maps coordinate using the legacy map link.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Legacy Coordinate Map Link](https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ll` | query | `string` | yes | Legacy center coordinate as latitude,longitude. |
| `q` | query | `string` | no | Optional label for the specified coordinate or address. |
| `z` | query | `number` | no | Legacy zoom level. |
| `t` | query | `string` | no | Legacy map type: m standard, k satellite, h hybrid, r transit. |
