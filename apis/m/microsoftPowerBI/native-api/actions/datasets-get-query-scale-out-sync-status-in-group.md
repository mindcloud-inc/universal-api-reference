# Get Query Scale Out Sync Status In Group with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/queryScaleOut/syncStatus`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Query Scale Out Sync Status In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-query-scale-out-sync-status-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
