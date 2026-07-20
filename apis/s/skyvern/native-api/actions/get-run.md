# Get Run with Skyvern

Retrieves task or workflow run details from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs/:run_id`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Get Run](https://www.skyvern.com/docs/api-reference/agent/get-a-run-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The task run or workflow run ID. |
