# List Workspace Users with Clockify

Lists all workspace users in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/users`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Users](https://docs.developer.clockify.me/#tag/User/operation/getUsersOfWorkspace)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier from Clockify. |
| `name` | query | `string` | no | Filter users by name. |
| `email` | query | `string` | no | Filter users by email. |
| `status` | query | `list<string>` | no | Filter users by status. Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `account-statuses` | query | `list<string>` | no | If provided, returns users filtered by account status. Accepted values: `ACTIVE`, `DELETED`, `LIMITED`, `LIMITED_DELETED`, `NOT_REGISTERED`, `PENDING_EMAIL_VERIFICATION`. Send multiple values as a string separated by `,`. |
| `project-id` | query | `string` | no | If provided, returns users that have access to the specified project. |
| `memberships` | query | `list<string>` | no | Include users along with workspaces, groups, or projects they have access to. Accepted values: `ALL`, `NONE`, `PROJECT`, `USERGROUP`, `WORKSPACE`. |
| `include-roles` | query | `boolean` | no | Include role information in response. |
