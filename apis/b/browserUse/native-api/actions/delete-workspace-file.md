# Delete Workspace File with Browser Use

Deletes a workspace file from Browser Use.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workspaces/:workspace_id/files`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Delete Workspace File](https://docs.browser-use.com/cloud/api-v3/workspaces/delete-workspace-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | Relative file path to delete. |
| `workspace_id` | path | `string` | yes | Workspace ID. |
