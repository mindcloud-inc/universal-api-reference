# List Tasks with Microsoft 365

Retrieves tasks from a Microsoft 365 task list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/todo/lists/{{taskListId}}/tasks`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Tasks](https://learn.microsoft.com/en-us/graph/api/todotasklist-list-tasks?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskListId` | path | `string` | yes | Microsoft To Do task list ID. |
| `$top` | query | `number` | no | — |
