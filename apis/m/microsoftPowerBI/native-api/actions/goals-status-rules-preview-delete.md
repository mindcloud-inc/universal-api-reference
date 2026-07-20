# Delete with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/statusRules`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete](https://learn.microsoft.com/en-us/rest/api/power-bi/goals-status-rules(preview)/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
