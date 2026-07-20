# Refresh Goal Current Value with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/RefreshGoalCurrentValue()`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Refresh Goal Current Value](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/refresh-goal-current-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
