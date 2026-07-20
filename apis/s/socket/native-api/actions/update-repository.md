# Update Repository with Socket

Updates an existing repository in Socket.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/repos/:repo_slug`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Update Repository](https://docs.socket.dev/reference/updateorgrepo)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `archived` | body | `boolean` | no |
| `default_branch` | body | `string` | no |
| `description` | body | `string` | no |
| `homepage` | body | `string` | no |
| `name` | body | `string` | yes |
| `visibility` | body | `string` | no |
| `workspace` | body | `string` | no |
| `workspace` | query | `string` | no |
| `repo_slug` | path | `string` | yes |
