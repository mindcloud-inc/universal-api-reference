# Run Task with Anchor

Creates a task run in Anchor.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/tasks/:taskId/run`
- **Base URL:** `https://api.anchorbrowser.io`
- **Official documentation:** [Run Task](https://docs.anchorbrowser.io/api-reference/tasks/run-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input_params` | body | `object` | yes |
| `taskId` | path | `string` | yes |
