# Abort Workflow Execution with Shuffler

Aborts a workflow execution in Shuffler.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/{workflowId}/executions/{executionId}/abort`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Abort Workflow Execution](https://shuffler.io/docs/API#abort-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `executionId` | path | `string` | yes | Execution Id path parameter. |
| `workflowId` | path | `string` | yes | Workflow Id path parameter. |
