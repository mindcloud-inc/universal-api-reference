# Update Task with Microsoft 365

Updates a task in Microsoft 365.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Update Task](https://learn.microsoft.com/en-us/graph/api/todotask-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskListId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
| `title` | body | `string` | no |
| `body.content` | body | `string` | no |
| `importance` | body | `string` | no |
| `status` | body | `string` | no |
