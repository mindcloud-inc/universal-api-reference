# List Child Nodes with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/node/:nodeId!children`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [List Child Nodes](https://api.smugmug.com/api/v2/doc/reference/node.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | SmugMug node identifier. |
