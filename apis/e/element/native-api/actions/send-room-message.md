# Send Room Message with Element

Creates a message in an Element room.

## Endpoint

- **Method:** `PUT`
- **Path:** `/_matrix/client/v3/rooms/:roomId/send/m.room.message/:txnId`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Send Room Message](https://spec.matrix.org/latest/client-server-api/#put_matrixclientv3roomsroomidsendeventtypetxnid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | Room ID that should receive the message. |
| `txnId` | path | `string` | yes | Client-generated transaction ID for idempotent message sends. |
| `body` | body | `string` | yes | Plain-text message body to send. |
| `msgtype` | body | `string` | no | Matrix message type. Defaults to m.text. |
