# Send Reminder with Blueink

Sends a reminder for a Blueink packet.

## Endpoint

- **Method:** `PUT`
- **Path:** `/packets/:packetId/remind/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Send Reminder](https://developer.blueink.com/api/#tag/Packet/operation/sendPacketReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packetId` | path | `string` | yes | Packet ID to send a reminder to. |
