# Add a user to a workspace or organization with Asana

Adds a user to an Asana workspace or organization.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspace_gid/addUser`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a user to a workspace or organization](https://developers.asana.com/reference/adduserforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.user` | body | `string` | yes | — |
| `workspace_gid` | path | `string` | yes | Asana workspace gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.user` | body | `string` | no | Asana user parameter. |
