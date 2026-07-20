# Get Node with AITable.ai

Retrieves a node from a space in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/nodes/:nodeId`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Get Node](https://developers.aitable.ai/api/reference/#get-node-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the node. |
| `nodeId` | path | `string` | yes | AITable node ID to retrieve. |
