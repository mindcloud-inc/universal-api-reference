# List Action Run Approvers with Port API AI

Retrieves action run approvers from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/actions/runs/:run_id/approvers`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [List Action Run Approvers](https://docs.port.io/api-reference/get-an-action-runs-approvers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_id` | path | `string` | yes | The action run identifier. |
