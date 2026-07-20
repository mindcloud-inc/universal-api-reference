# Get By ID with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/get-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
| `timestamp` | path | `date` | yes | The timestamp for the value of the goal |
| `$expand` | query | `string` | no | Accepts a comma-separated list of data types, which will be expanded inline in the response. Supports notes. |
