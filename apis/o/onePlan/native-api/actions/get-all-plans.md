# Get All Plans with OnePlan

Retrieves plans from OnePlan.

## Endpoint

- **Method:** `GET`
- **Path:** `/workplan`
- **Base URL:** `https://my.oneplan.ai/api`
- **Official documentation:** [Get All Plans](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan_FilterField_FilterValue_ShowArchived_ShowTemplates_BuiltInField_EditOnly)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BuiltInField` | query | `string` | no | Optional built-in field query parameter from the docs. |
| `EditOnly` | query | `string` | no | Optional edit-only query parameter from the docs. |
| `FilterField` | query | `string` | no | Optional filter field query parameter from the docs. |
| `FilterValue` | query | `string` | no | Optional filter value query parameter from the docs. |
| `ShowArchived` | query | `string` | no | Optional flag to include archived plans. |
| `ShowTemplates` | query | `string` | no | Optional flag to include templates. |
