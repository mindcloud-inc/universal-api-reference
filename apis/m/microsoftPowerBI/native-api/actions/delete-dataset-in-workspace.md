# Delete Dataset in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Dataset in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/delete-dataset-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `datasetId` | path | `string` | yes | The dataset ID to delete. |
