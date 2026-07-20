# Get Task with Process Street

## Endpoint

- **Method:** `GET`
- **Path:** `/workflow-runs/:workflowRunId/tasks/:taskId`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Get Task](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/GET/workflow-runs/{workflowRunId}/tasks/{taskId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `taskId` | path | `string` | yes | The ID of the task. |
