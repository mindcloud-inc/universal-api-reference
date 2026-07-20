# Report Problem By Address with Apple Map Links

Opens Apple Maps problem reporting by address.

## Endpoint

- **Method:** `GET`
- **Path:** `/report-a-problem`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Report Problem By Address](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | yes | Problem report location as an address string. |
