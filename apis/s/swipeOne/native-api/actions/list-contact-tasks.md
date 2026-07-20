# List Contact Tasks with Swipe One

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/contacts/:contactId/tasks`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [List Contact Tasks](https://docs.swipeone.com/en/articles/10546025-tasks#h_ac22398bff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace to list contact tasks from. |
| `contactId` | path | `string` | yes | Contact whose tasks should be listed. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page. |
