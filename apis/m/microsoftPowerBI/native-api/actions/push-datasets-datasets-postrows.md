# Datasets PostRows with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/tables/[:tableName]/rows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Datasets PostRows](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `tableName` | path | `string` | yes | The table name |
| `rows[]` | body | `array<object>` | no | An array of data rows pushed to a dataset table. Each element is a collection of properties represented using key-value format. |
