# Delete Task with Microsoft 365

Deletes a task from Microsoft 365.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Delete Task](https://learn.microsoft.com/en-us/graph/api/todotask-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskListId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
