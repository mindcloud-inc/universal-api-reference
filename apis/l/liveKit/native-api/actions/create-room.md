# Create Room with LiveKit

Creates a new room in LiveKit.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/CreateRoom`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Create Room](https://docs.livekit.io/reference/other/roomservice-api/#createroom)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the room to create. |
| `empty_timeout` | body | `number` | no | Seconds to keep the room open if no one joins. |
| `departure_timeout` | body | `number` | no | Seconds the room remains open after the last participant leaves. |
| `max_participants` | body | `number` | no | Maximum participant count; 0 means no limit. |
| `metadata` | body | `string` | no | Initial room metadata. |
