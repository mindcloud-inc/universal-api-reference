# Get queue with UiPath Orchestrator

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/QueueDefinitions(:id)`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Get queue](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric queue definition ID. |
