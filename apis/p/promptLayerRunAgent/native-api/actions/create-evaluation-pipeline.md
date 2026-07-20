# Create Evaluation Pipeline with PromptLayer Run Agent

Creates a new evaluation pipeline in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Evaluation Pipeline](https://docs.promptlayer.com/reference/create-reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_group_id` | body | `number` | yes | ID of the dataset group to use. |
| `name` | body | `string` | no | Name for the pipeline. If omitted, PromptLayer auto-generates one. |
| `dataset_version_number` | body | `number` | no | Specific dataset version to use. Uses latest if omitted. |
