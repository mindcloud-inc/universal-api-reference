# Get Refresh Execution Details with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `datasets/[:datasetId]/refreshes/[:refreshId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Refresh Execution Details](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-execution-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `refreshId` | path | `string` | yes | The refresh ID |
