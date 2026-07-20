# Get details of a specific sending node with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/mumara/sending-nodes/{nodeId}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get details of a specific sending node](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | Sending node UUID |
| `userId` | query | `string` | yes | MongoDB User ID for authorization |
