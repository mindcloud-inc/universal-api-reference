# Report Problem By Place ID with Apple Map Links

Opens Apple Maps problem reporting by Place ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/report-a-problem`
- **Base URL:** `https://maps.apple.com`
- **Official documentation:** [Report Problem By Place ID](https://developer.apple.com/documentation/mapkit/unified-map-urls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `place-id` | query | `string` | yes | Apple Maps Place ID for the reported location. |
