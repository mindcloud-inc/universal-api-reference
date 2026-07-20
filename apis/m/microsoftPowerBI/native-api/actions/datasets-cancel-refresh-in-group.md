# Cancel Refresh In Group with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/refreshes/[:refreshId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Cancel Refresh In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/cancel-refresh-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `refreshId` | path | `string` | yes | The refresh ID |
