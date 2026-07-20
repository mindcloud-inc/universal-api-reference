# Unassign Workflow Run User with Process Street

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflow-runs/:workflowRunId/assignees/:email`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Unassign Workflow Run User](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/DELETE/workflow-runs/{workflowRunId}/assignees/{email})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `email` | path | `string` | yes | The email address to unassign. |
