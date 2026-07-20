# List Workflow Users with SigningHub

Retrieves workflow users from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/workflow/users`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [List Workflow Users](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_GetWorkflowUsers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package whose workflow users should be returned. |
