# Wait for Task with CloudConvert

Waits for a CloudConvert task to finish.

## Endpoint

- **Method:** `GET`
- **Path:** `https://sync.api.cloudconvert.com/v2/tasks/:id/wait`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Wait for Task](https://cloudconvert.com/docs/api-reference/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CloudConvert task ID. |
