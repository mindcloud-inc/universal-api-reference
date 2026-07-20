# Get Action Run Logs with Port API AI

Retrieves action run logs from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/runs/:run_id/logs`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Action Run Logs](https://docs.port.io/api-reference/get-an-actions-run-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The Port action run identifier. |
