# Add User to Workspace with Clockify

Adds a user to a workspace in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/users`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Add User to Workspace](https://docs.developer.clockify.me/#tag/Workspace/operation/addUsers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `send-email` | query | `string` | yes |
| `email` | body | `string` | yes |
