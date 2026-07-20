# Update Workspace with Airiam AI

Updates an existing workspace in Airiam AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspaceId`
- **Base URL:** `https://platform.sectorflow.ai`
- **Official documentation:** [Update Workspace](https://docs.ai.airiam.com/reference/workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace identifier. |
| `name` | body | `string` | no | Updated workspace name. |
| `description` | body | `string` | no | Updated workspace description. |
