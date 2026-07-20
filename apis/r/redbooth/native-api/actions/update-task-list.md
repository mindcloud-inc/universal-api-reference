# Update Task List with Redbooth

Updates an existing task list in Redbooth.

## Endpoint

- **Method:** `PUT`
- **Path:** `/task_lists/:id`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Update Task List](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Redbooth task list ID |
| `name` | body | `string` | yes | Updated task list name |
