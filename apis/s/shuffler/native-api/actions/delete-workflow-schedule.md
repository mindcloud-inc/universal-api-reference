# Delete Workflow Schedule with Shuffler

Deletes a workflow schedule from Shuffler.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflows/{workflowId}/schedule/{scheduleId}`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Delete Workflow Schedule](https://shuffler.io/docs/API#stop-a-workflow-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scheduleId` | path | `string` | yes | Schedule Id path parameter. |
| `workflowId` | path | `string` | yes | Workflow Id path parameter. |
