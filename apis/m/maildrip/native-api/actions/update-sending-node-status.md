# Update sending node status with Maildrip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/mumara/sending-nodes/{nodeId}/status`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Update sending node status](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | Sending node UUID |
| `userId` | body | `string` | yes | MongoDB User ID |
| `status` | body | `number` | yes | New status (0=inactive, 1=active) |
