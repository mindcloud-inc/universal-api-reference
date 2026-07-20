# Delete Embedded Link with AITable.ai

Deletes an existing embedded link from AITable.ai.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks/:linkId`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Delete Embedded Link](https://developers.aitable.ai/api/reference/#delete-embedded-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the node. |
| `nodeId` | path | `string` | yes | AITable node ID containing the embedded link. |
| `linkId` | path | `string` | yes | Embedded link ID to delete. |
