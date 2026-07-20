# Update Workflow Node Run with Port API AI

Updates a workflow node run in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workflows/nodes/runs/:node_run_identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Workflow Node Run](https://docs.port.io/api-reference/update-a-workflow-node-run)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `node_run_identifier` | path | `string` | yes | The workflow node run identifier. |
| `status` | body | `string` | yes | Node run status. |
| `result` | body | `string` | yes | Node run result. |
