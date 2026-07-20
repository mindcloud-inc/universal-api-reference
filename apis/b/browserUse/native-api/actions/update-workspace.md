# Update Workspace with Browser Use

Updates an existing workspace in Browser Use.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspace_id`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Update Workspace](https://docs.browser-use.com/cloud/api-v3/workspaces/update-workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional workspace name. |
| `workspace_id` | path | `string` | yes | Workspace ID. |
