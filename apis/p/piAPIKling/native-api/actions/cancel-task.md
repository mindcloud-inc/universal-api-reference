# Cancel Task with PiAPI/Kling

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/task/:task_id`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Cancel Task](https://piapi.ai/docs/kling-api/cancel-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The pending PiAPI task ID to cancel. |
