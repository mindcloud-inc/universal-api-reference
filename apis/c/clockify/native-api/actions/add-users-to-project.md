# Add Users to Project with Clockify

Adds users to a project in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/projects/:projectId/memberships`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Add Users to Project](https://docs.developer.clockify.me/#tag/Project/operation/addUsersToProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userGroups.contains` | body | `list<string>` | no | Accepted values: `CONTAINS`, `DOES_NOT_CONTAIN`. |
| `userGroups.ids[]` | body | `array<string>` | no | — |
| `userGroups.status` | body | `list<string>` | no | Accepted values: `ACTIVE`, `ALL`, `INACTIVE`. |
| `workspaceId` | path | `list<string>` | yes | — |
| `projectId` | path | `string` | yes | — |
| `remove` | body | `boolean` | no | — |
| `userGroups` | body | `object` | no | — |
| `userIds[]` | body | `array<string>` | no | — |
