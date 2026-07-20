# Set All Dataset Connections In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/Default.SetAllConnections`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Set All Dataset Connections In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/set-all-dataset-connections-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `connectionString` | body | `string` | yes | A dataset connection string |
