# Run Workflow with Unstructured

Runs a workflow in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/:workflow_id/run`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Run Workflow](https://docs.unstructured.io/api-reference/workflows/run-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow ID. |
