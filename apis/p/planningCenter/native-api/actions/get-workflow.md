# Get Workflow with Planning Center

Retrieves a workflow from Planning Center.

## Endpoint

- **Method:** `GET`
- **Path:** `/people/v2/workflows/:id`
- **Base URL:** `https://api.planningcenteronline.com`
- **Official documentation:** [Get Workflow](https://api.planningcenteronline.com/docs/apps/people/versions/2025-11-10/vertices/workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Workflow ID |
| `include` | query | `string` | no | Include associated resources |
