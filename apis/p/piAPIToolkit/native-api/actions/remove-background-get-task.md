# Remove Background - Get Task with PiAPI/Toolkit

Retrieves a background-removal task from PiAPI/Toolkit by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/{task_id}`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Remove Background - Get Task](https://piapi.ai/docs/remove-background/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | PiAPI task identifier returned by a create-task or history response. |
