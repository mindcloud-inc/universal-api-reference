# Update Refresh Schedule with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/dataflows/[:dataflowId]/refreshSchedule`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Refresh Schedule](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/update-refresh-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dataflowId` | path | `string` | yes | The dataflow ID |
| `value` | body | `object` | yes | An object that contains the details of a refresh schedule |
