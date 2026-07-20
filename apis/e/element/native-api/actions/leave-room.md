# Leave Room with Element

Leaves a room in Element for the current user.

## Endpoint

- **Method:** `POST`
- **Path:** `/_matrix/client/v3/rooms/:roomId/leave`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Leave Room](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3roomsroomidleave)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to leave. |
