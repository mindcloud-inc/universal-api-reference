# Share Document Package with SigningHub

Shares a document package in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/workflow`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Share Document Package](https://manuals.nsignhub.com/latest/Api/#tag/Document-Package/operation/V4_Workflow_StartWorkflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package to be shared. |
