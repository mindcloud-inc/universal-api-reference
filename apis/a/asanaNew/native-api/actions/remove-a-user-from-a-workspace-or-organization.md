# Remove a user from a workspace or organization with Asana

Removes a user from an Asana workspace or organization.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspace_gid/removeUser`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a user from a workspace or organization](https://developers.asana.com/reference/removeuserforworkspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `data.user` | body | `string` | yes | — |
| `workspace_gid` | path | `string` | yes | Path parameter: workspace_gid |
