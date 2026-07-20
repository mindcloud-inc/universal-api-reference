# Mark Notification Read with ProjectManager

Marks a notification as read in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/notifications/:id/markread`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Mark Notification Read](https://developer.projectmanager.com/api-reference/notification/mark-notification-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the notification to mark read |
