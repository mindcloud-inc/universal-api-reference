# List Notifications with Yanado

Retrieves notifications from Yanado by type.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-api/notifications/:type`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [List Notifications](https://api.yanado.com/docs/#get-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | path | `string` | yes | Notification type from the Yanado path parameter. |
| `anyUser` | query | `boolean` | no | Return notifications for any user. |
| `listId` | query | `string` | no | Limit notifications to one list. |
