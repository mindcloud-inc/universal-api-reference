# Delete Room with LiveKit

Deletes an existing room from LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/DeleteRoom`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Delete Room](https://docs.livekit.io/reference/other/roomservice-api/#deleteroom)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | body | `string` | yes | Name of the room to delete. |
