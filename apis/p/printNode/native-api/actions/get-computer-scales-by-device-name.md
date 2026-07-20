# Get Computer Scales by Device Name with PrintNode

Retrieves scales by device name for a computer from PrintNode.

## Endpoint

- **Method:** `GET`
- **Path:** `/computer/:computerId/scales/:deviceName`
- **Base URL:** `https://api.printnode.com`
- **Official documentation:** [Get Computer Scales by Device Name](https://www.printnode.com/en/docs/api/curl#scales-http)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `computerId` | path | `string` | yes | PrintNode computer ID. |
| `deviceName` | path | `string` | yes | Scale device name from PrintNode. |
