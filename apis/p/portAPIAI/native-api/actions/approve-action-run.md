# Approve Action Run with Port API AI

Approves an action run in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/actions/runs/:run_id/approval`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Approve Action Run](https://docs.port.io/api-reference/approve-an-action-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The Port action run identifier. |
| `status` | body | `string` | yes | Approval decision |
