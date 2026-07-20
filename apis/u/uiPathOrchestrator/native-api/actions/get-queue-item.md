# Get queue item with UiPath Orchestrator

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/QueueItems(:id)`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Get queue item](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric queue item ID. |
