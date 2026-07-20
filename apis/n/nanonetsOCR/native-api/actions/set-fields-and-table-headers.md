# Set Fields And Table Headers with Nanonets OCR

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflows/:workflow_id/fields`
- **Base URL:** `https://app.nanonets.com/api/v4`
- **Official documentation:** [Set Fields And Table Headers](https://apidocs.nanonets.com/docs/api/workflow-management/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `list` | yes | Workflow identifier. |
| `fields[]` | body | `array<object>` | yes | Array of field objects with name values. |
| `table_headers[]` | body | `array<object>` | no | Array of table header objects with name values. |
