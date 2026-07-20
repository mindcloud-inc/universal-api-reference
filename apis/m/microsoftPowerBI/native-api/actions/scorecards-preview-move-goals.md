# Move Goals with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/MoveGoals()`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Move Goals](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/move-goals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalToMove` | body | `object` | yes | The rank validation information for the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newNext` | body | `object` | no | Optional. The rank validation information for the new next-sibling of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newParent` | body | `object` | no | Optional. The rank validation information for the new parent of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
| `newPrevious` | body | `object` | no | Optional. The rank validation information for the new previous-sibling of the goal to be moved. The caller provides validation information to confirm that they know the existing position of a goal within the hierarchy of goals. |
