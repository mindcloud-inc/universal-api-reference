# Create Task List with Redbooth

Creates a new task list in Redbooth.

## Endpoint

- **Method:** `POST`
- **Path:** `/task_lists`
- **Base URL:** `https://redbooth.com/api/3`
- **Official documentation:** [Create Task List](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-list-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Task list name |
| `project_id` | body | `number` | yes | Parent project ID |
