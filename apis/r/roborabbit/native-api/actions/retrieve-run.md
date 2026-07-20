# Retrieve Run with Roborabbit

Retrieves a run for a specific Roborabbit task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/:task_uid/runs/:uid`
- **Base URL:** `https://api.roborabbit.com`
- **Official documentation:** [Retrieve Run](https://developers.roborabbit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_uid` | path | `string` | yes | The parent task UID. |
| `uid` | path | `string` | yes | The run UID from Roborabbit. |
