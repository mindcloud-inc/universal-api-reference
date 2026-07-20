# Update Workspace with Rossum

Updates a workspace in Rossum.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Update Workspace](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Updated workspace name. |
| `workspaceID` | path | `number` | yes | Rossum workspace ID. |
