# List Parent Nodes with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/node/:nodeId!parents`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [List Parent Nodes](https://api.smugmug.com/api/v2/doc/reference/node.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeId` | path | `string` | yes | SmugMug node identifier. |
