# Search Workspace Users with Clockify

Finds workspace users in Clockify by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/users/info`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Search Workspace Users](https://docs.developer.clockify.me/#tag/User/operation/filterUsersOfWorkspace)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier from Clockify. |
| `name` | body | `string` | no | Filter users by name. |
| `email` | body | `string` | no | Filter users by email. |
| `status` | body | `list<string>` | no | Filter by workspace membership statuses. Accepted values: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `accountStatuses` | body | `list<string>` | no | Filter by account statuses. Accepted values: `ACTIVE`, `DELETED`, `LIMITED`, `LIMITED_DELETED`, `NOT_REGISTERED`, `PENDING_EMAIL_VERIFICATION`. Send multiple values as a array. |
| `include-roles` | body | `boolean` | no | Include role information in response. |
| `memberships` | body | `list<string>` | no | Filter by memberships. Accepted values: `ALL`, `NONE`, `PROJECT`, `USERGROUP`, `WORKSPACE`. |
| `project-id` | body | `string` | no | Filter by project ID. |
