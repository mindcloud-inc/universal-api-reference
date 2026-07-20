# Remove Subscribers From Segment with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/segment/:segId/remove`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Remove Subscribers From Segment](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-remove-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segId` | path | `string` | yes | PushAlert segment ID. |
| `subscribers` | body | `string` | yes | JSON array string of subscriber IDs to remove from the segment. |
