# Get Room State with Element

Retrieves a room's state from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/rooms/:roomId/state`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Room State](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomidstate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to inspect. |
