# Create Segment with Campaign Monitor

Creates a new segment in Campaign Monitor.

## Endpoint

- **Method:** `POST`
- **Path:** `/segments/:listId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Create Segment](https://www.campaignmonitor.com/api/v3-3/segments/#creating-a-segment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Campaign Monitor list identifier. |
| `Title` | body | `string` | yes | Title of the segment. |
