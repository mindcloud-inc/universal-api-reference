# Get Computer Scale with PrintNode

Retrieves a specific scale from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/computer/:computerId/scale/:deviceName/:deviceNumber`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Get Computer Scale](https://www.printnode.com/en/docs/api/curl#scales-http)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerId` | path | `string` | yes | PrintNode computer ID. |
| `deviceName` | path | `string` | yes | Scale device name from PrintNode. |
| `deviceNumber` | path | `string` | yes | Scale device number from PrintNode. |
