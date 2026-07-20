# Get Run Timeline with Skyvern

Retrieves timeline events for a run from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/runs/:run_id/timeline`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Get Run Timeline](https://www.skyvern.com/docs/api-reference/agent/get-run-timeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The workflow run or task run ID. |
