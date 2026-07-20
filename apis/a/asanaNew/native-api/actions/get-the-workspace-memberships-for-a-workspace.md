# Get the workspace memberships for a workspace with Asana

Retrieves workspace memberships for a workspace from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/workspace_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get the workspace memberships for a workspace](https://developers.asana.com/reference/getworkspacemembershipsforworkspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes |
