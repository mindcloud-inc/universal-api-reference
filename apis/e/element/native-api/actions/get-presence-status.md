# Get Presence Status with Element

Retrieves a user's presence status from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/presence/:userId/status`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Presence Status](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3presenceuseridstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Matrix user ID to inspect. |
