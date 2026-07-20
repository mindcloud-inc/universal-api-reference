# Set All Dataset Connections with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/Default.SetAllConnections`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Set All Dataset Connections](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/set-all-dataset-connections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `connectionString` | body | `string` | yes | A dataset connection string |
