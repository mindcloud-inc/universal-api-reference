# Create Report with Sunwise

Creates a new report in Sunwise.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports/create-report`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Create Report](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `history_id` | body | `string` | yes |
| `report_name` | body | `string` | yes |
| `project_id` | body | `string` | yes |
