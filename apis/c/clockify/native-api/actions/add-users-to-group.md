# Add Users to Group with Clockify

Adds users to a group in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/user-groups/:userGroupId/users`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Add Users to Group](https://docs.developer.clockify.me/#tag/Group/operation/addUser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `userGroupId` | path | `string` | yes |
| `userId` | body | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
