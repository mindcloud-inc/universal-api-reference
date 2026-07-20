# Get Task with PiAPI/Trellis

Retrieves a task from PiAPI/Trellis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/:task_id`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Task](https://piapi.ai/docs/trellis-api/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | PiAPI task ID returned by a create-task response. |
