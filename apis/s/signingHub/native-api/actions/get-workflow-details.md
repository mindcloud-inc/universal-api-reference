# Get Workflow Details with SigningHub

Retrieves workflow details from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/workflow`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Get Workflow Details](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_GetWorkflowDetail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package whose workflow details should be returned. |
