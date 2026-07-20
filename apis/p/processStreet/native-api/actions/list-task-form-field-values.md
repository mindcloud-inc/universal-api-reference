# List Task Form Field Values with Process Street

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow-runs/:workflowRunId/tasks/:taskId/form-fields`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [List Task Form Field Values](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-field-values/GET/workflow-runs/{workflowRunId}/tasks/{taskId}/form-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `taskId` | path | `string` | yes | The ID of the task. |
