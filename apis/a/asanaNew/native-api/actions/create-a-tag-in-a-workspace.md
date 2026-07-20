# Create a tag in a workspace with Asana

Creates a tag in an Asana workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspace_gid/tags`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a tag in a workspace](https://developers.asana.com/reference/createtagforworkspace)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data` | body | `string` | yes |
| `workspace_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
