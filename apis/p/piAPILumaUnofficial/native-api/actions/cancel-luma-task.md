# Cancel Luma Task with PiAPI/Luma (unofficial)

Cancels an existing Luma task in PiAPI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/task/:task_id`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Cancel Luma Task](https://piapi.ai/docs/dream-machine/cancel-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Pending Luma task identifier to cancel. |
