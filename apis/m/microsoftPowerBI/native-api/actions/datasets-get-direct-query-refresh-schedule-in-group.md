# Get Direct Query Refresh Schedule In Group with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/directQueryRefreshSchedule`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Direct Query Refresh Schedule In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-direct-query-refresh-schedule-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
