# Add Column To Evaluation Pipeline with PromptLayer Run Agent

Adds a column to a PromptLayer evaluation pipeline.

## Endpoint

- **Method:** `POST`
- **Path:** `/report-columns`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Add Column To Evaluation Pipeline](https://docs.promptlayer.com/reference/add-report-columns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_id` | body | `number` | yes | ID of the evaluation pipeline report. |
| `column_type` | body | `string` | yes | Type of evaluation column to add. |
| `name` | body | `string` | yes | Display name for the column. |
| `configuration` | body | `object` | yes | Column-type-specific configuration object. |
| `position` | body | `number` | no | Optional position for the column. |
| `is_part_of_score` | body | `boolean` | no | Whether to include this column in default score calculation. |
