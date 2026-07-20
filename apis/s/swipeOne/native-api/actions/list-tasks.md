# List Tasks with Swipe One

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/tasks`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [List Tasks](https://docs.swipeone.com/en/articles/10546025-tasks#h_6ad4d3fe4c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace to list tasks from. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page. |
| `status` | query | `string` | no | Optional task status filter. |
| `assignedTo` | query | `string` | no | Optional assignee filter. |
