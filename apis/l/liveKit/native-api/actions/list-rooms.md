# List Rooms with LiveKit

Retrieves rooms from LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/ListRooms`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [List Rooms](https://docs.livekit.io/reference/other/roomservice-api/#listrooms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `names[]` | body | `array<string>` | no | Optional list of room names to return. |
