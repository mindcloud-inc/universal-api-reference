# List Workflow Run Assignees with Process Street

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow-runs/:workflowRunId/assignees`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [List Workflow Run Assignees](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/GET/workflow-runs/{workflowRunId}/assignees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
