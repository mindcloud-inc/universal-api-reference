# Run Workflow with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/workflows/:workflowId/run`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Run Workflow](https://docs.kadoa.com/api-reference/workflows/run-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow ID |
| `variables` | body | `string` | no | JSON object of runtime variables |
