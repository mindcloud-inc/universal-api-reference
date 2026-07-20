# Get Scorecard By Report Id with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/scorecards/GetScorecardByReportId(reportId=[:reportId])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get Scorecard By Report Id](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/get-scorecard-by-report-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `reportId` | path | `string` | yes | The ID of the internal report associated with the scorecard |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports goals, goalValues, and aggregations. |
