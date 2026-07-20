# List Dataset Datasources with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/datasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Dataset Datasources](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasources-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `datasetId` | path | `string` | yes | The dataset ID. |
