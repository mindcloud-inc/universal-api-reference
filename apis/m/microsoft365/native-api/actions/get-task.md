# Get Task with Microsoft 365

Retrieves a task from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Get Task](https://learn.microsoft.com/en-us/graph/api/todotask-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskListId` | path | `string` | yes |
| `taskId` | path | `string` | yes |
