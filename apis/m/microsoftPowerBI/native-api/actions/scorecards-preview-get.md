# Get with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/scorecards`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `$top` | query | `number` | no | Returns only the first n results. |
