# Get Task with PiAPI/MMAudio

Retrieves an MMAudio task from PiAPI/MMAudio.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/{task_id}`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Task](https://piapi.ai/docs/mmaudio-api/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The PiAPI task_id returned when you create the MMAudio task. |
