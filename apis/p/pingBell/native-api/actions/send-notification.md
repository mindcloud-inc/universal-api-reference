# Send Notification with PingBell

Creates a notification for a specific PingBell.

## Endpoint

- **Method:** `POST`
- **Path:** `/log`
- **Base URL:** `https://app.pingbell.io`
- **Official documentation:** [Send Notification](https://pingbell.io/docs/pingbell-api/post-notifications/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The PingBell ID from the PingBell log URL. |
