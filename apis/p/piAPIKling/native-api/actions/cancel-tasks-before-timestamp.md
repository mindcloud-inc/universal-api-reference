# Cancel Tasks Before Timestamp with PiAPI/Kling

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/tasks`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Cancel Tasks Before Timestamp](https://piapi.ai/docs/kling-api/cancel-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_before` | query | `number` | yes | Unix timestamp in seconds. Cancel pending Kling tasks created before this time. |
