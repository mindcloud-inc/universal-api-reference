# Update Refresh Schedule with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `datasets/[:datasetId]/refreshSchedule`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Refresh Schedule](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-refresh-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID |
| `value` | body | `object` | yes | An object that contains the details of a refresh schedule |
