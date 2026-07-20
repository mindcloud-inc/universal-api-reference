# Datasets DeleteRows with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `datasets/[:datasetId]/tables/[:tableName]/rows`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Datasets DeleteRows](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-delete-rows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `tableName` | path | `string` | yes | The table name |
