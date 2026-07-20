# Update a workspace with Asana

Updates a workspace in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspace_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a workspace](https://developers.asana.com/reference/updateworkspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `workspace_gid` | path | `string` | yes |
