# Get Task with PiAPI/Wanx

Retrieves a task from PiAPI/Wanx by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/[:task_id]`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Task](https://piapi.ai/docs/wanx-api/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | WanX task ID returned when you create a task. |
