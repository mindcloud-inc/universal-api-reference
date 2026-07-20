# Get a workspace with Asana

Retrieves a workspace from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a workspace](https://developers.asana.com/reference/getworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes | Asana workspace gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
