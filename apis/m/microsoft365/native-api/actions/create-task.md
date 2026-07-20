# Create Task with Microsoft 365

Creates a new task in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/todo/lists/{{taskListId}}/tasks`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Task](https://learn.microsoft.com/en-us/graph/api/todotasklist-post-tasks?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskListId` | path | `string` | yes |
| `title` | body | `string` | yes |
| `body.content` | body | `string` | no |
| `importance` | body | `string` | no |
