# List Notifications with Bluesky

Retrieves notifications for the current Bluesky account.

## Endpoint

- **Method:** `GET`
- **Path:** `/xrpc/app.bsky.notification.listNotifications`
- **Base URL:** `{pdsUrl}`
- **Official documentation:** [List Notifications](https://docs.bsky.app/docs/api/app-bsky-notification-list-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of notifications to return. |
| `cursor` | query | `string` | no | Cursor for the next page of notifications. |
