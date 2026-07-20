# List Tasks With Emails Attached with Yanado

Retrieves tasks with attached emails from Yanado.

## Endpoint

- **Method:** `GET`
- **Path:** `/public-api/email-tasks`
- **Base URL:** `https://api.yanado.com`
- **Official documentation:** [List Tasks With Emails Attached](https://api.yanado.com/docs/#get-tasks-with-emails-attached)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | query | `string` | no | Filter tasks by list ID. |
| `assignee` | query | `string` | no | Filter tasks by assignee. |
| `statusId` | query | `string` | no | Filter tasks by status ID. |
| `query` | query | `string` | no | Search tasks by query text. |
