# Get Skyreels Task with PiAPI/Skyreels

Retrieves a Skyreels task by ID from PiAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/task/:task_id`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [Get Skyreels Task](https://piapi.ai/docs/skyreels-api/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | Skyreels task identifier returned from Create Skyreels Task. |
