# Send Push Notification with ActivitySmith

Sends a push notification in ActivitySmith.

## Endpoint

- **Method:** `POST`
- **Path:** `/push-notification`
- **Base URL:** `https://activitysmith.com/api`
- **Official documentation:** [Send Push Notification](https://activitysmith.com/docs/api-reference/endpoint/push-notification)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `message` | body | `string` | no |
| `media` | body | `string` | no |
| `redirection` | body | `string` | no |
| `target` | body | `object` | no |
| `target.channels[]` | body | `array<string>` | no |
