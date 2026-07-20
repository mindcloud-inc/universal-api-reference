# Update Segment with Maildroppa

## Endpoint

- **Method:** `PUT`
- **Path:** `/subscriber/segment/{subscriberSegmentId}`
- **Base URL:** `https://api.maildroppa.com`
- **Official documentation:** [Update Segment](https://api.maildroppa.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expression` | body | `object` | no | Filter expression defining the segment criteria. |
| `name` | body | `string` | no | Display name for the segment. |
| `subscriberSegmentId` | path | `string` | yes | Unique identifier of the segment to update. |
