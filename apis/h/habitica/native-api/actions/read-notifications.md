# Read Notifications with Habitica

Marks notifications as read in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/notifications/read`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Read Notifications](https://habitica.com/apidoc/#api-Notification-ReadNotifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notificationIds` | body | `list<string>` | yes | The Habitica notification IDs to mark as read. |
