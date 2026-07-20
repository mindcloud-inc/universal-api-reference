# Approve or Reject Task with Process Street

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflow-runs/:workflowRunId/approvals`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Approve or Reject Task](https://public-api.process.st/api/v1.1/docs/index.html#tag/tasks/PUT/workflow-runs/{workflowRunId}/approvals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `approvalTaskId` | body | `string` | yes | The ID of the approval task. |
| `subjectTaskId` | body | `string` | no | Optional subject task ID to approve or reject. |
| `status` | body | `string` | yes | Whether to approve or reject the task. |
| `comment` | body | `string` | no | Optional comment for the approval decision. |
