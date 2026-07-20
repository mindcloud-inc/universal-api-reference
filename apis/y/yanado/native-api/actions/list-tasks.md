# List Tasks with Yanado

Retrieves tasks from Yanado.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-api/tasks`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [List Tasks](https://api.yanado.com/docs/#get-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | query | `string` | no | Filter tasks by list ID. |
| `assignee` | query | `string` | no | Filter tasks by assignee. |
| `statusId` | query | `string` | no | Filter tasks by status ID. |
| `query` | query | `string` | no | Search tasks by query text. |
