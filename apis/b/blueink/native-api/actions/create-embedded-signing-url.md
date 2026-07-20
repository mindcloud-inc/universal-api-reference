# Create Embedded Signing URL with Blueink

Creates an embedded signing URL for a Blueink packet.

## Endpoint

- **Method:** `POST`
- **Path:** `/packets/:packetId/embed_url/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Create Embedded Signing URL](https://developer.blueink.com/api/#tag/Packet/operation/createPacketEmbedURL)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packetId` | path | `string` | yes | Packet ID to generate an embedded signing URL for. |
