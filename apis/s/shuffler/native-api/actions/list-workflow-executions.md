# List Workflow Executions with Shuffler

Retrieves workflow executions from Shuffler.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/{workflowId}/executions`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [List Workflow Executions](https://shuffler.io/docs/API#list-workflow-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow Id path parameter. |
