# Delete By ID with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/delete-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
