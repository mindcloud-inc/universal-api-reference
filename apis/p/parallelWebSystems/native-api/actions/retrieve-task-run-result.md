# Retrieve Task Run Result with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks/runs/:run_id/result`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [Retrieve Task Run Result](https://docs.parallel.ai/api-reference/tasks-v1/retrieve-task-run-result)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The Parallel task run ID. |
| `timeout` | query | `number` | no | Maximum seconds to wait for the task run result. |
