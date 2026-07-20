# Update Workspace Model with Airiam AI

Updates a workspace model in Airiam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspaceId/:modelId`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Update Workspace Model](https://docs.ai.airiam.com/reference/workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace identifier. |
| `modelId` | path | `string` | yes | Model identifier. |
| `added` | body | `boolean` | yes | Whether the model should be added to the workspace. |
