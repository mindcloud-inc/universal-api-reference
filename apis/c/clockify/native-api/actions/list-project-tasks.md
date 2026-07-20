# List Project Tasks with Clockify

Lists all project tasks in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/projects/:projectId/tasks`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List Project Tasks](https://docs.developer.clockify.me/#tag/Task/operation/getTasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `projectId` | path | `string` | yes |
| `name` | query | `string` | no |
| `strict-name-search` | query | `boolean` | no |
| `is-active` | query | `boolean` | no |
