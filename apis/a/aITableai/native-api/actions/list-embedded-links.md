# List Embedded Links with AITable.ai

Retrieves embedded links for a node in AITable.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [List Embedded Links](https://developers.aitable.ai/api/reference/#get-list-of-embedded-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the node. |
| `nodeId` | path | `string` | yes | AITable node ID whose embedded links should be listed. |
