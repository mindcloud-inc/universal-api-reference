# Get teams in a workspace with Asana

Retrieves teams in an Asana workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/teams`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get teams in a workspace](https://developers.asana.com/reference/getteamsforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `workspace_gid` | path | `string` | yes | Path parameter: workspace_gid |
