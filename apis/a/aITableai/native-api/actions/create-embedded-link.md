# Create Embedded Link with AITable.ai

Creates a new embedded link in AITable.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/fusion/v1/spaces/:spaceId/nodes/:nodeId/embedlinks`
- **Base URL:** `https://aitable.ai`
- **Official documentation:** [Create Embedded Link](https://developers.aitable.ai/api/reference/#create-embedded-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | AITable space ID containing the node. |
| `nodeId` | path | `string` | yes | AITable node ID for the embedded link. |
| `payload` | body | `object` | yes | Embedded link request body from AITable. Use the fields required by the AITable embedded link endpoint. |
