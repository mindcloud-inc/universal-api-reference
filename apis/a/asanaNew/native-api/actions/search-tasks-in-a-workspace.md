# Search tasks in a workspace with Asana

Finds tasks in an Asana workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/tasks/search`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Search tasks in a workspace](https://developers.asana.com/reference/searchtasksforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | query | `string` | no | Performs a full-text search on both task name and description. |
| `opt_fields[]` | query | `array<string>` | no | This endpoint returns a compact resource, excluding most properties by default. To include properties, set this query parameter to a comma-separated list of the properties you wish to include. Send multiple values as a array. |
| `workspace_gid` | path | `string` | yes | Path parameter: workspace_gid |
| `workspace_guid` | path | `string` | yes | Globally unique identifier for the workspace or organization. |
| `projects.any` | query | `string` | no | Comma-separated list of project IDs. When paired with Search, returns tasks in Any of the provided Project IDs. |
| `projects.any` | query | `string` | no | — |
