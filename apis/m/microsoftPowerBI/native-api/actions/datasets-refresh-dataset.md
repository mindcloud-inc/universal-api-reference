# Refresh Dataset with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/refreshes`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Refresh Dataset](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/refresh-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `notifyOption` | body | `object` | yes | Mail notification options. This parameter is not applicable to enhanced refreshes or API operations with a service principal. |
| `applyRefreshPolicy` | body | `boolean` | no | Determine if the policy is applied or not |
| `commitMode` | body | `object` | no | Determines if objects will be committed in batches or only when complete |
| `effectiveDate` | body | `date` | no | If an incremental refresh policy is applied, the effectiveDate parameter overrides the current date. |
| `maxParallelism` | body | `number` | no | The maximum number of threads on which to run parallel processing commands |
| `objects[]` | body | `array<object>` | no | An array of objects to be processed |
| `retryCount` | body | `number` | no | Number of times the operation will retry before failing. Temporary internal errors may trigger a retry of the refresh, even when this parameter is set to 0. |
| `timeout` | body | `string` | no | 2[0-3]):[0-5][0-9]:[0-5][0-9]$ |
| `type` | body | `object` | no | The type of processing to perform |
