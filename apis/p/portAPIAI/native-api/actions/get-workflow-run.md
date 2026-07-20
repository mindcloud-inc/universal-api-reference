# Get Workflow Run with Port API AI

Retrieves a workflow run from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/runs/:identifier`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Workflow Run](https://docs.port.io/api-reference/get-a-workflow-run-by-identifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The workflow run identifier. |
