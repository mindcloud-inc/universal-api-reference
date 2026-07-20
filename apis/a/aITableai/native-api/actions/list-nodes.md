# List Nodes with AITable.ai

Retrieves nodes from a space in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/nodes`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Nodes](https://developers.aitable.ai/api/reference/#get-node-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nodeType` | query | `string` | no | Optional node type filter when listing nodes. |
| `spaceId` | path | `string` | yes | AITable space ID whose root nodes should be listed. |
