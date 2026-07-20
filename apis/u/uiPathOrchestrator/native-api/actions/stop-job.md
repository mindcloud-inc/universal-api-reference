# Stop job with UiPath Orchestrator

## Endpoint

- **Method:** `POST`
- **Path:** `/odata/Jobs/UiPath.Server.Configuration.OData.StopJob`
- **Base URL:** `https://cloud.uipath.com/{organizationName}/{tenantName}/orchestrator_`
- **Official documentation:** [Stop job](https://docs.uipath.com/orchestrator/automation-cloud/latest/api-guide/jobs-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | body | `number` | yes | The numeric job ID to stop. |
| `strategy` | body | `string` | yes | The stop strategy, such as Kill or Stop. |
