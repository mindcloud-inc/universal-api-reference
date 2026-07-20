# Edit Evaluation Pipeline Column with PromptLayer Run Agent

Updates a column in a PromptLayer evaluation pipeline.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/report-columns/:reportColumnId`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Edit Evaluation Pipeline Column](https://docs.promptlayer.com/reference/edit-report-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportColumnId` | path | `number` | yes | ID of the report column to edit. |
| `report_id` | body | `number` | yes | ID of the evaluation pipeline report. |
| `column_type` | body | `string` | yes | Column type for the existing column. |
| `name` | body | `string` | yes | Updated display name for the column. |
| `configuration` | body | `object` | yes | Updated column configuration. |
| `is_part_of_score` | body | `boolean` | no | Whether the column should count toward the default score. |
