# List Participants with LiveKit

Retrieves participants in a LiveKit room.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/ListParticipants`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [List Participants](https://docs.livekit.io/reference/other/roomservice-api/#listparticipants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | body | `string` | yes | Name of the room whose participants should be listed. |
