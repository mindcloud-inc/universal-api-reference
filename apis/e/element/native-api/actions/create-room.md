# Create Room with Element

Creates a room in Element.

## Endpoint

- **Method:** `POST`
- **Path:** `/_matrix/client/v3/createRoom`
- **Base URL:** `{homeserverUrl}`
- **Official documentation:** [Create Room](https://spec.matrix.org/latest/client-server-api/#post_matrixclientv3createroom)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional room name for the new room. |
