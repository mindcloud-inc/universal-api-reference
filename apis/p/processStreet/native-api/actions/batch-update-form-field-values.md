# Batch Update Form Field Values with Process Street

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow-runs/:workflowRunId/form-fields`
- **Base URL:** `https://public-api.process.st/api/v1.1`
- **Official documentation:** [Batch Update Form Field Values](https://public-api.process.st/api/v1.1/docs/index.html#tag/form-field-values/POST/workflow-runs/{workflowRunId}/form-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowRunId` | path | `string` | yes | The ID of the workflow run. |
| `fields[]` | body | `array<object>` | no | Form field values to update. |
| `fields[].id` | body | `string` | yes | The ID of the form field value to update. |
| `fields[].value` | body | `string` | no | Single value for the form field. |
| `fields[].values[]` | body | `array<string>` | no | Multiple values for the form field. |
| `fields[].timeHidden` | body | `boolean` | no | Whether to hide the time portion for date fields. |
| `fields[].dataSetRowId` | body | `string` | no | Optional data set row ID for linked dropdowns. |
