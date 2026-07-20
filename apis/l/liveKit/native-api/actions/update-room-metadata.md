# Update Room Metadata with LiveKit

Updates metadata for an existing LiveKit room.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/UpdateRoomMetadata`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Update Room Metadata](https://docs.livekit.io/reference/other/roomservice-api/#updateroommetadata)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `room` | body | `string` | yes |
| `metadata` | body | `string` | yes |
