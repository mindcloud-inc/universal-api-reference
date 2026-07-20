# Save Default Segment with Leadboxer

Updates default segment assignments for users in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/segment/preference`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Save Default Segment](https://developers.leadboxer.com/reference/savedefaultsegment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | query | `string` | yes |
| `datasetId` | body | `string` | yes |
| `segmentId` | body | `number` | yes |
| `users[]` | body | `array<number>` | no |
