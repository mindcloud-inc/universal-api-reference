# Cancel Refresh with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `datasets/[:datasetId]/refreshes/[:refreshId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Cancel Refresh](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/cancel-refresh)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `refreshId` | path | `string` | yes | The refresh ID |
