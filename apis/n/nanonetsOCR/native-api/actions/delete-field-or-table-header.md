# Delete Field Or Table Header with Nanonets OCR

## Endpoint

- **Method:** `DELETE`
- **Path:** `/workflows/:workflow_id/fields/:field_id`
- **Base URL:** `https://app.nanonets.com/api/v4`
- **Official documentation:** [Delete Field Or Table Header](https://apidocs.nanonets.com/docs/api/workflow-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `list` | yes | Workflow ID that owns the field or table header. |
| `field_id` | path | `string` | yes | Field or table header ID to delete. |
