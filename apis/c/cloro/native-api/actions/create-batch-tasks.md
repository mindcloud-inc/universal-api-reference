# Create Batch Tasks with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/async/task/batch`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Create Batch Tasks](https://docs.cloro.dev/api-reference/endpoint/create-batch-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tasks[]` | body | `array<object>` | yes | Array of async task definitions to create in one batch. |
