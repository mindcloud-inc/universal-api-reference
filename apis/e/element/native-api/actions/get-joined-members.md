# Get Joined Members with Element

Retrieves joined room members from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/rooms/:roomId/joined_members`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Joined Members](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomidjoined_members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to inspect. |
