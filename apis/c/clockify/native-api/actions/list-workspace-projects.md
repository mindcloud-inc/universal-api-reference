# List Workspace Projects with Clockify

Lists all workspace projects in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/projects`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Workspace Projects](https://docs.developer.clockify.me/#tag/Project/operation/getProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | Workspace identifier. |
| `name` | query | `string` | no | Filter projects by name. |
| `strict-name-search` | query | `boolean` | no | Return exact project name matches only. |
| `archived` | query | `boolean` | no | Filter archived projects. |
| `billable` | query | `boolean` | no | Filter billable projects. |
| `clients[]` | query | `array<string>` | no | Filter by client IDs. |
| `contains-client` | query | `boolean` | no | Include or exclude matching clients. |
| `client-status` | query | `string` | no | Filter by client status. |
| `users[]` | query | `array<string>` | no | Filter by user IDs. |
| `contains-user` | query | `boolean` | no | Include or exclude matching users. |
| `user-status` | query | `string` | no | Filter by user status. |
| `is-template` | query | `boolean` | no | Filter template projects. |
| `hydrated` | query | `boolean` | no | Include hydrated project data. |
| `access` | query | `string` | no | Project access visibility. |
| `expense-limit` | query | `number` | no | Maximum expenses to include. |
| `expense-date` | query | `string` | no | Include expenses before this date (yyyy-MM-dd). |
| `userGroups[]` | query | `array<string>` | no | Filter by user group IDs. |
| `contains-group` | query | `boolean` | no | Include or exclude matching user groups. |
