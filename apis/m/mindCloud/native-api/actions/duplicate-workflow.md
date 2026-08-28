# Duplicate Workflow with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/workflows/:workflowId/duplicate`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Duplicate Workflow](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for this MindCloud v2 request. |
| `workflowId` | path | `string` | yes | Workflow ID for this MindCloud v2 request. |
