# Set Presence Status with Element

Updates a user's presence status in Element.

## Endpoint

- **Method:** `PUT`
- **Path:** `/_matrix/client/v3/presence/:userId/status`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Set Presence Status](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3presenceuseridstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Matrix user ID to update. |
| `presence` | body | `string` | yes | Presence state to publish. |
| `status_msg` | body | `string` | no | Optional status message to publish. |
