# Delete Task with Datalyse

Deletes an existing task from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/tasks/delete.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Delete Task](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | ID of the task to delete |
