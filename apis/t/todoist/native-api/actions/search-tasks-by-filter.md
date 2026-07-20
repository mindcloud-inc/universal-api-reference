# Search Tasks By Filter with Todoist

Finds tasks in Todoist by filter query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/tasks/filter`
- **Base URL:** `https://api.todoist.com`
- **Official documentation:** [Search Tasks By Filter](https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_tasks_by_filter_api_v1_tasks_filter_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Filter query string |
