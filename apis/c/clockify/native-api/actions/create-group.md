# Create Group with Clockify

Creates a new user group in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/user-groups`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Group](https://docs.developer.clockify.me/#tag/Group/operation/createUserGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `workspaceId` | path | `list<string>` | yes |
