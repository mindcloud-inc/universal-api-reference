# Add Subscribers To Segment with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/segment/:segId/add`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Add Subscribers To Segment](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-add-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segId` | path | `string` | yes | PushAlert segment ID. |
| `subscribers` | body | `string` | yes | JSON array string of subscriber IDs to add to the segment. |
