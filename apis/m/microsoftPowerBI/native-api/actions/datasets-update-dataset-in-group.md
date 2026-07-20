# Update Dataset In Group with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Dataset In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-dataset-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `queryScaleOutSettings` | body | `object` | no | Query scale-out settings of a dataset |
| `targetStorageMode` | body | `string` | no | The dataset storage mode |
