# Update Direct Query Refresh Schedule with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `datasets/[:datasetId]/directQueryRefreshSchedule`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Direct Query Refresh Schedule](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-direct-query-refresh-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `value` | body | `object` | yes | An object containing the refresh schedule details for DirectQuery or LiveConnection |
