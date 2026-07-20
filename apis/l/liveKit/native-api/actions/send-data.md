# Send Data with LiveKit

Sends data to participants in a LiveKit room.

## Endpoint

- **Method:** `POST`
- **Path:** `/twirp/livekit.RoomService/SendData`
- **Base URL:** `{livekitUrl}`
- **Official documentation:** [Send Data](https://docs.livekit.io/reference/other/roomservice-api/#senddata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | body | `string` | yes | — |
| `data` | body | `string` | yes | Raw data payload to send. Provide the payload expected by your LiveKit client data handler. |
| `kind` | body | `string` | yes | Delivery mode, usually reliable or lossy. |
| `destination_identities[]` | body | `array<string>` | no | — |
| `topic` | body | `string` | no | — |
