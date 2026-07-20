# Patch By ID with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])/notes([:noteId])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-notes(preview)/patch-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
| `timestamp` | path | `date` | yes | The timestamp for the value of the goal |
| `noteId` | path | `string` | yes | The unique identifier of the goal check-in note |
| `body` | body | `string` | yes | The note text |
