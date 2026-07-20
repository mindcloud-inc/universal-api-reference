# Update Segment with Campaign Monitor

Updates an existing segment in Campaign Monitor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/segments/:segmentId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Update Segment](https://www.campaignmonitor.com/api/v3-3/segments/#updating-a-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segmentId` | path | `string` | yes | Campaign Monitor segment identifier. |
| `Title` | body | `string` | yes | Title of the segment. |
