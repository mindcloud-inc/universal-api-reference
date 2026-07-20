# Get Repository with Socket

Retrieves detailed repository data from Socket.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/:org_slug/repos/:repo_slug`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Get Repository](https://docs.socket.dev/reference/getorgrepo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace` | query | `string` | no |
| `repo_slug` | path | `string` | yes |
