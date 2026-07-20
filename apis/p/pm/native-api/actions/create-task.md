# Create Task with 5pm

Creates a new task in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/tasks/add`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Create Task](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task[name]` | query | `string` | yes | Name of the task to create. |
