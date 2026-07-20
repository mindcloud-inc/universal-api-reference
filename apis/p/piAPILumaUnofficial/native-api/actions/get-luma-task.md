# Get Luma Task with PiAPI/Luma (unofficial)

Retrieves a Luma task from PiAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/:task_id`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Luma Task](https://piapi.ai/docs/dream-machine/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Luma task identifier returned by Create Luma Task. |
