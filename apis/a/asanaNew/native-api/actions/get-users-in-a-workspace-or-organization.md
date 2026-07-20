# Get users in a workspace or organization with Asana

Retrieves users in an Asana workspace or organization.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/users`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get users in a workspace or organization](https://developers.asana.com/reference/getusersforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes | Asana workspace gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
