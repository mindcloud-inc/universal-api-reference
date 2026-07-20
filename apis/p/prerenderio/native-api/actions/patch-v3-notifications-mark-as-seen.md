# Update Notifications Mark As Seen with Prerender.io

Updates notifications as seen in Prerender.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v3/notifications/mark-as-seen`
- **Base URL:** `https://api.prerender.io`
- **Official documentation:** [Update Notifications Mark As Seen](https://api.prerender.io/v3/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loginUserNotificationIds` | body | `list<string>` | yes |
