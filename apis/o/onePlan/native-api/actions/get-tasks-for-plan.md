# Get Tasks For Plan with OnePlan

Retrieves tasks for a plan from OnePlan.

## Endpoint

- **Method:** `GET`
- **Path:** `/workplan/{id}/tasks`
- **Base URL:** `https://my.oneplan.ai/api`
- **Official documentation:** [Get Tasks For Plan](https://my.oneplan.ai/ApiHelp/Api/GET-api-workplan-id-tasks_HasUpdates_FilterField_FilterValue_BuiltInField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BuiltInField` | query | `string` | no | Optional built-in field query parameter from the docs. |
| `FilterField` | query | `string` | no | Optional filter field query parameter from the docs. |
| `FilterValue` | query | `string` | no | Optional filter value query parameter from the docs. |
| `HasUpdates` | query | `string` | no | Optional flag to filter tasks with updates. |
| `id` | path | `string` | yes | Plan identifier from the path. |
