# List Runs with Roborabbit

Retrieves runs for a specific Roborabbit task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/:task_uid/runs`
- **Base URL:** `https://api.roborabbit.com`
- **Official documentation:** [List Runs](https://developers.roborabbit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for paginated run results. |
| `task_uid` | path | `string` | yes | The task UID from Roborabbit. |
