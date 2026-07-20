# Update Workspace with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/workspaces/:workspaceId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Workspace](https://docs.fingertip.com/openapi-specs/update-workspace.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | ID of the workspace to update. |
| `name` | body | `string` | no | Updated workspace name. |
