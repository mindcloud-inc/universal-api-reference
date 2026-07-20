# Add Action Run Log with Port API AI

Creates an action run log in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/runs/:run_id/logs`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Add Action Run Log](https://docs.port.io/api-reference/add-a-log-to-an-action-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The Port action run identifier. |
| `message` | body | `string` | yes | Log message to append to the action run |
