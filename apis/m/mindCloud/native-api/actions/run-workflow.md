# Run Workflow with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/workflows/:workflowId/run`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Run Workflow](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | body | `string` | no | Environment ID for this MindCloud v2 request. |
| `version` | body | `string` | no | Version for this MindCloud v2 request. |
| `workflowId` | path | `string` | yes | Workflow ID for this MindCloud v2 request. |
