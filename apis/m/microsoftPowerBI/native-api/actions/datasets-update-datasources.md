# Update Datasources with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/Default.UpdateDatasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Datasources](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-datasources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `updateDetails[]` | body | `array<object>` | yes | An array of data source connection update requests |
