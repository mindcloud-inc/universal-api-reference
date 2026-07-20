# Update Datasources In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/Default.UpdateDatasources`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Datasources In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-datasources-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | Dataset Id. |
| `updateDetails[]` | body | `array<object>` | yes | An array of data source connection update requests |
