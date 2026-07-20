# Retrieve Notifications with ProjectManager

Retrieves notifications from ProjectManager.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/data/notifications`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Retrieve Notifications](https://developer.projectmanager.com/api-reference/notification/retrieve-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastId` | query | `string` | no | To continue loading more notifications in a series of requests, provide the ID of the oldest notification from the currently loaded batch as the `lastId` parameter |
| `senderId` | query | `string` | no | Filter the notifications to only those sent by the user with the specified ID |
| `notificationTypes[]` | query | `array<string>` | no | Specifies the types of notifications to return.  If not provided, all notifications will be returned. |
| `asFlatList` | query | `boolean` | no | If set to true all notifications will be returned as a flat list, otherwise they will be grouped by parent in the same manner as displayed in the UI. |
