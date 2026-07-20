# Set Typing Indicator with Element

Updates a room's typing indicator in Element.

## Endpoint

- **Method:** `PUT`
- **Path:** `/_matrix/client/v3/rooms/:roomId/typing/:userId`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Set Typing Indicator](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3roomsroomidtypinguserid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to update. |
| `userId` | path | `string` | yes | Matrix user ID whose typing state should be updated. |
| `typing` | body | `boolean` | yes | Whether the user is currently typing. |
| `timeout` | body | `number` | no | Optional timeout in milliseconds for the typing notice. |
