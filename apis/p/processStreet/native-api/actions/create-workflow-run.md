# Create Workflow Run with Process Street

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow-runs`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Create Workflow Run](https://public-api.process.st/api/v1.1/docs/index.html#tag/workflow-runs/POST/workflow-runs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | body | `string` | yes | The ID of the workflow to run. |
| `name` | body | `string` | no | The name of the new workflow run. |
| `dueDate` | body | `date` | no | Optional due date for the new workflow run. |
| `shared` | body | `boolean` | no | Whether the workflow run should be shared. |
