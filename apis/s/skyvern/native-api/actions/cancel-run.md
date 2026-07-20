# Cancel Run with Skyvern

Cancels a task or workflow run in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/runs/:run_id/cancel`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Cancel Run](https://www.skyvern.com/docs/api-reference/agent/cancel-a-run-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The task run or workflow run ID to cancel. |
