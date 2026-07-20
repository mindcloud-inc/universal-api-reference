# Update Refresh Schedule In Group with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/datasets/[:datasetId]/refreshSchedule`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Refresh Schedule In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-refresh-schedule-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `datasetId` | path | `string` | yes | The dataset ID |
| `value` | body | `object` | yes | An object that contains the details of a refresh schedule |
