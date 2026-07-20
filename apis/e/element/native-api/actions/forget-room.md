# Forget Room with Element

Forgets a room in Element for the current user.

## Endpoint

- **Method:** `POST`
- **Path:** `/_matrix/client/v3/rooms/:roomId/forget`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Forget Room](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3roomsroomidforget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to forget. |
