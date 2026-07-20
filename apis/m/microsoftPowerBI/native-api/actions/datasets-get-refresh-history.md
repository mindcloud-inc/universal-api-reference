# Get Refresh History with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `datasets/[:datasetId]/refreshes`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Refresh History](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `$top` | query | `number` | no | The requested number of entries in the refresh history. If not provided, the default is the last available 60 entries. |
