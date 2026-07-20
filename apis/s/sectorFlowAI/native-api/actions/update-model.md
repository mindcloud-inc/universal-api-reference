# Update Model with SectorFlow.AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/models/{modelId}`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Update Model](https://docs.sectorflowai.com/reference/models)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modelId` | path | `string` | yes | The ID of the model to update. |
| `modelRequest` | body | `object` | yes | The updated model details documented by SectorFlow as ModelRequest. |
