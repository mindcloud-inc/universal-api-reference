# Get task with UiPath Orchestrator

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/Tasks(:id)`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Get task](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/tasks-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric task ID. |
