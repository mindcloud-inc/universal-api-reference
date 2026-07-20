# Create queue with UiPath Orchestrator

## Endpoint

- **Method:** `POST`
- **Path:** `/odata/QueueDefinitions`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Create queue](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/queue-items-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Queue name. |
| `Description` | body | `string` | no | Queue description. |
