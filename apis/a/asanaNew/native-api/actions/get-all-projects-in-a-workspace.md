# Get all projects in a workspace with Asana

Retrieves all projects in an Asana workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/projects`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get all projects in a workspace](https://developers.asana.com/reference/getprojectsforworkspace)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `archived` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
