# Update User Notification with Zeplin

Updates an existing user notification in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/me/notifications/{notification_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update User Notification](https://docs.zeplin.dev/reference/updateusernotification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notification_id` | path | `string` | yes | Notification id |
| `is_read` | body | `boolean` | yes | New is_read status for notifications |
