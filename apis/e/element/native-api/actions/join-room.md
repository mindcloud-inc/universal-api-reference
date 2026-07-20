# Join Room with Element

Joins a room in Element by ID or alias.

## Endpoint

- **Method:** `POST`
- **Path:** `/_matrix/client/v3/join/:roomIdOrAlias`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Join Room](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3joinroomidoralias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomIdOrAlias` | path | `string` | yes | Room ID or canonical alias to join. |
