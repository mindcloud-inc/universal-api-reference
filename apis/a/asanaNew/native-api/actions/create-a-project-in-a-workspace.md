# Create a project in a workspace with Asana

Creates a project in an Asana workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspace_gid/projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a project in a workspace](https://developers.asana.com/reference/createprojectforworkspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `object` | yes |
| `workspace_gid` | path | `string` | yes |
