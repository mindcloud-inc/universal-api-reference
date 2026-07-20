# Update Packet with Blueink

Updates an existing packet in Blueink.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/packets/:packetId/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Update Packet](https://developer.blueink.com/api/#tag/Packet/operation/updatePacket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packetId` | path | `string` | yes | Packet ID to update. |
| `name` | body | `string` | no | Updated signer name. |
| `suppress_reminder` | body | `boolean` | no | Whether to suppress reminder notifications for this signer. |
