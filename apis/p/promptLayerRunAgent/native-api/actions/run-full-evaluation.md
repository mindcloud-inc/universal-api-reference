# Run Full Evaluation with PromptLayer Run Agent

Runs a full evaluation in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports/:reportId/run`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Run Full Evaluation](https://docs.promptlayer.com/reference/run-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportId` | path | `number` | yes | ID of the evaluation pipeline report to run. |
| `name` | body | `string` | yes | Name of the final report to be created. |
| `dataset_id` | body | `number` | no | Dataset ID to use for the report. If omitted, uses the pipeline default dataset. |
| `refresh_dataset` | body | `boolean` | no | Whether to refresh the dataset before running the report. |
