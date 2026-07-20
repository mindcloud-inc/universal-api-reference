# Send Notification with PushAlert

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/v2/web-push/send`
- **Base URL:** `https://api.pushalert.co`
- **Official documentation:** [Send Notification](https://pushalert.co/documentation/rest-api-v2/web-push#rest-api-send-notification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action1` | body | `string` | no | JSON string with title and url for the first CTA button. |
| `action1_attr` | body | `string` | no | JSON string with title and url template for the first CTA button. |
| `action2` | body | `string` | no | JSON string with title and url for the second CTA button. |
| `action2_attr` | body | `string` | no | JSON string with title and url template for the second CTA button. |
| `attributes` | body | `string` | no | Single JSON object string used to target subscribers by custom attribute. |
| `audience_id` | body | `string` | no | Audience Creator ID for precise targeting. |
| `expire_time` | body | `string` | no | Notification expiry time in seconds. |
| `icon` | body | `string` | no | HTTPS icon URL for the notification. |
| `large_image` | body | `string` | no | HTTPS hero image URL for the notification. |
| `message_attr` | body | `string` | no | Notification message template using subscriber attributes. |
| `schedule_time` | body | `string` | no | Unix timestamp for scheduled delivery. |
| `subscriber` | body | `string` | no | Single subscriber ID to target. |
| `subscribers` | body | `string` | no | JSON array string of subscriber IDs to target. |
| `timezone_schedule` | body | `string` | no | ISO datetime for timezone-aware scheduling. |
| `title` | body | `string` | yes | Notification title. |
| `title_attr` | body | `string` | no | Notification title template using subscriber attributes. |
| `url_attr` | body | `string` | no | Destination URL template using subscriber attributes. |
| `message` | body | `string` | yes | Notification message body. |
| `url` | body | `string` | yes | Destination URL when the notification is clicked. |
