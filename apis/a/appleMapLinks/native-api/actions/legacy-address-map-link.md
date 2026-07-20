# Legacy Address Map Link with Apple Map Links

Shows an Apple Maps address using the legacy map link.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Legacy Address Map Link](https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Legacy address string to show on the map. |
| `q` | query | `string` | no | Optional label for the specified address. |
