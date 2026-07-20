# Send Notification with Pushinator

Creates a new notification in a Pushinator channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications/send`
- **Base URL:** `https://api.pushinator.com/api/v2`
- **Official documentation:** [Send Notification](https://pushinator.com/api#send-notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | body | `string` | yes | The Pushinator channel ID that will receive the notification. |
| `content` | body | `string` | yes | The notification text to send. |
| `acknowledgment_required` | body | `boolean` | no | Whether subscribers must acknowledge the notification. |
