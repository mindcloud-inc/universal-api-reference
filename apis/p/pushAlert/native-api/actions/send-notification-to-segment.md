# Send Notification To Segment with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/segment/:segId/send`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Send Notification To Segment](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-segment-send-notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `icon` | body | `string` | no | HTTPS icon URL for the notification. |
| `segId` | path | `string` | yes | PushAlert segment ID. |
| `title` | body | `string` | yes | Notification title. |
| `message` | body | `string` | yes | Notification message body. |
| `url` | body | `string` | yes | Destination URL when the notification is clicked. |
