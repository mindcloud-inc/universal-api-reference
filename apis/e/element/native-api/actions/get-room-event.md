# Get Room Event with Element

Retrieves a room event from Element.

## Endpoint

- **Method:** `GET`
- **Path:** `/_matrix/client/v3/rooms/:roomId/event/:eventId`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Get Room Event](https://spec.matrix.org/latest/client-server-api/#get_matrixclientv3roomsroomideventeventid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID to inspect. |
| `eventId` | path | `string` | yes | Event ID to fetch. |
