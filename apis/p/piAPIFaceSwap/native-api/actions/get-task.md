# Get Task with PiAPI/FaceSwap

Retrieves a task from PiAPI/FaceSwap by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/{task_id}`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Task](https://piapi.ai/docs/faceswap-api/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The PiAPI task identifier to retrieve. |
