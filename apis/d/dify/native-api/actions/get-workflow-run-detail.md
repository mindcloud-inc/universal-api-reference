# Get Workflow Run Detail with Dify

Retrieves workflow run details from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/run/:workflow_run_id`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Get Workflow Run Detail](https://docs.dify.ai/api-reference/workflow-runs/get-workflow-run-detail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_run_id` | path | `string` | yes | Workflow run ID to inspect. |
