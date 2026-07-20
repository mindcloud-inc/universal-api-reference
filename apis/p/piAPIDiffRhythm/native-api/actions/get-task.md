# Get Task with PiAPI/DiffRhythm

Retrieves a DiffRhythm task from PiAPI/DiffRhythm.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/{task_id}`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Task](https://piapi.ai/docs/diffrhythm/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The PiAPI task ID returned when you created the DiffRhythm generation task. |
