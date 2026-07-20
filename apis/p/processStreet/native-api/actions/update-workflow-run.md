# Update Workflow Run with Process Street

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflow-runs/:workflowRunId`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Update Workflow Run](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/PUT/workflow-runs/{workflowRunId})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `name` | body | `string` | yes | The workflow run name. |
| `status` | body | `string` | yes | The workflow run status. |
| `shared` | body | `boolean` | yes | Whether the workflow run is shared. |
| `dueDate` | body | `date` | no | Optional due date for the workflow run. |
