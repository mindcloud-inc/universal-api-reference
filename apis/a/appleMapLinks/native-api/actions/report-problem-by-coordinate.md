# Report Problem By Coordinate with Apple Map Links

Opens Apple Maps problem reporting by coordinate.

## Endpoint

- **Method:** `GET`
- **Path:** `/report-a-problem`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Report Problem By Coordinate](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `coordinate` | query | `string` | yes | Problem report location as latitude,longitude. |
