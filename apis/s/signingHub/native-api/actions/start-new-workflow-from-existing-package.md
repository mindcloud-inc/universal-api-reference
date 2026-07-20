# Start New Workflow From Existing Package with SigningHub

Creates a new workflow from an existing package in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/workflow/new`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Start New Workflow From Existing Package](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_Package_StartNewWorkflowFromExisting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the existing document package. |
