# Cancel Luma Tasks with PiAPI/Luma (unofficial)

Cancels Luma tasks in PiAPI created before a timestamp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Cancel Luma Tasks](https://piapi.ai/docs/dream-machine/cancel-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `number` | yes | Cancel pending Luma tasks created before this Unix timestamp. |
