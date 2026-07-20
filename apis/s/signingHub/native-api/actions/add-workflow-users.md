# Add Workflow Users with SigningHub

Adds users to a workflow in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/workflow/users`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Add Workflow Users](https://manuals.nsignhub.com/latest/Api/#tag/Document-Workflow/operation/V4_Workflow_WorkflowAddUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | SigningHub package ID, which the recipients are to be added to. |
| `users[]` | body | `array<object>` | yes | One or more workflow users to add. |
