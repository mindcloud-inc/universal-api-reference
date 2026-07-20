# Trigger Query Scale Out Sync with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `datasets/[:datasetId]/queryScaleOut/sync`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Trigger Query Scale Out Sync](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/trigger-query-scale-out-sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
