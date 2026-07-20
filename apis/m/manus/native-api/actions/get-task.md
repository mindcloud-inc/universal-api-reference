# Get Task with Manus

Retrieves a task from Manus by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:task_id`
- **Base URL:** `https://api.manus.ai/v1`
- **Official documentation:** [Get Task](https://open.manus.ai/docs/v1/get-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | path | `string` | yes | The ID of the task to retrieve |
| `convert` | query | `boolean` | no | Whether to convert the task result to a structured response |
