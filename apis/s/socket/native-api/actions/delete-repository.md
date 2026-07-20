# Delete Repository with Socket

Deletes an existing repository from Socket.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/orgs/:org_slug/repos/:repo_slug`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Delete Repository](https://docs.socket.dev/reference/deleteorgrepo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | query | `string` | no |
| `repo_slug` | path | `string` | yes |
