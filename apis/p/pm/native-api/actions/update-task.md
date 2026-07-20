# Update Task with 5pm

Updates an existing task in 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/tasks/update`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Update Task](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task[id]` | query | `string` | yes | Unique identifier of the task. |
