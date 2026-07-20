# Get with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/statusRules`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Get](https://learn.microsoft.com/en-us/rest/api/power-bi/goals-status-rules(preview)/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
