# Execute Workflow with Shuffler

Creates a workflow execution in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/{workflowId}/execute`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Execute Workflow](https://shuffler.io/docs/API#execute-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `execution_argument` | body | `string` | no | Optional execution payload. |
| `start` | body | `string` | no | Optional start node. |
| `workflowId` | path | `string` | yes | Workflow Id path parameter. |
