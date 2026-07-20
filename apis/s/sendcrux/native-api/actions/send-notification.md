# Send Notification with Sendcrux

Creates a notification event in Sendcrux.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/notification`
- **Base URL:** `https://sendcrux.com`
- **Official documentation:** [Send Notification](https://api.sendbound.com/notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounce_type` | body | `string` | no | The bounce subtype when `type=bounced`. |
| `description` | body | `string` | no | A human-readable explanation for the notification event. |
| `message_id` | body | `string` | yes | The provider message identifier associated with the delivery event. |
| `report_type` | body | `string` | no | The report type when `type=abuse` or `type=spam`. |
| `type` | body | `string` | yes | The notification type, such as sent, bounced, abuse, spam, or failed. |
