# Trigger Query Scale Out Sync In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/queryScaleOut/sync`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Trigger Query Scale Out Sync In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/trigger-query-scale-out-sync-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
