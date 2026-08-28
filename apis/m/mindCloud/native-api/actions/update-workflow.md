# Update Workflow with MindCloud

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/workflows/:workflowId`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Update Workflow](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isActive` | body | `boolean` | no | Is Active for this MindCloud v2 request. |
| `name` | body | `string` | no | Name for this MindCloud v2 request. |
| `tags[]` | body | `array<string>` | no | Tags for this MindCloud v2 request. |
| `workflowId` | path | `string` | yes | Workflow ID for this MindCloud v2 request. |
