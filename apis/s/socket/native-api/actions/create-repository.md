# Create Repository with Socket

Creates a new repository in Socket.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/:org_slug/repos`
- **Base URL:** `https://api.socket.dev/v0`
- **Official documentation:** [Create Repository](https://docs.socket.dev/reference/createorgrepo)

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
