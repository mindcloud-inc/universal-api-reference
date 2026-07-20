# Post with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Post](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
| `timestamp` | body | `date` | yes | The UTC timestamp of the goal value check-in. The time portion of the timestamp is zero. |
| `forecast` | body | `number` | no | Optional. The value trend forecast of the goal. |
| `status` | body | `number` | no | Optional. The goal status ID. |
| `target` | body | `number` | no | Optional. The target value of the goal. |
| `trend` | body | `number` | no | Optional. The value trend of the goal. |
| `value` | body | `number` | no | Optional. The current value of the goal. |
