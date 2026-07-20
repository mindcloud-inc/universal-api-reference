# Retrieve Packet Certificate of Evidence with Blueink

Retrieves a packet certificate of evidence from Blueink.

## Endpoint

- **Method:** `GET`
- **Path:** `/packets/:packetId/coe/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [Retrieve Packet Certificate of Evidence](https://developer.blueink.com/api/#tag/Packet/operation/getPacketCOE)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packetId` | path | `string` | yes | Packet ID to retrieve the certificate of evidence for. |
