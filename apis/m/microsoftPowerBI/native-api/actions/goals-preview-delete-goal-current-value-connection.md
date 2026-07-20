# Delete Goal Current Value Connection with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/DeleteGoalCurrentValueConnection()`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Goal Current Value Connection](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/delete-goal-current-value-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
