# Get Task with DomoAI

Retrieves task status and outputs from DomoAI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/[:taskId]`
- **Base URL:** `https://api.domoai.com`
- **Official documentation:** [Get Task](https://docs.domoai.app/api-reference/task/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The DomoAI task ID to retrieve. |
