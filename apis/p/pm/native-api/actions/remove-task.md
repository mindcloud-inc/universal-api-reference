# Remove Task with 5pm

Deletes an existing task from 5pm.

## Endpoint

- **Method:** `POST`
- **Path:** `/service/post/tasks/remove`
- **Base URL:** `{workspaceUrl}/api/v2`
- **Official documentation:** [Remove Task](https://www.5pmweb.com/help/api_docs.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Unique identifier of the task. |
