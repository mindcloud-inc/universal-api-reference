# Update Dataset with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `datasets/[:datasetId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Dataset](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `queryScaleOutSettings` | body | `object` | no | Query scale-out settings of a dataset |
| `targetStorageMode` | body | `string` | no | The dataset storage mode |
