# List Tasks with Todoist

Retrieves tasks from Todoist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [List Tasks](https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_tasks_api_v1_tasks_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | — |
| `section_id` | query | `string` | no | — |
| `label` | query | `string` | no | — |
| `filter` | query | `string` | no | Natural language filter query for selecting tasks. |
| `ids` | query | `list<string>` | no | Comma-separated task IDs to fetch specific tasks. |
| `parent_id` | query | `string` | no | — |
