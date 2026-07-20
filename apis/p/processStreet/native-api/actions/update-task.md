# Update Task with Process Street

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflow-runs/:workflowRunId/tasks/:taskId`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Update Task](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/PUT/workflow-runs/{workflowRunId}/tasks/{taskId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `taskId` | path | `string` | yes | The ID of the task. |
| `status` | body | `string` | yes | The task status. |
| `dueDate` | body | `date` | no | Optional due date for the task. |
