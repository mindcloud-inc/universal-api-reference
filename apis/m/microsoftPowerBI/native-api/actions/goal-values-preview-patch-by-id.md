# Patch By ID with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/patch-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
| `timestamp` | path | `date` | yes | The timestamp for the value of the goal |
| `createdTime` | body | `date` | no | The UTC time at creation |
| `forecast` | body | `number` | no | The goal value trend forecast |
| `lastModifiedTime` | body | `date` | no | The UTC time at last modification |
| `notes[]` | body | `array<object>` | no | The notes for the goal |
| `status` | body | `number` | no | The ID of the goal status |
| `target` | body | `number` | no | The goal target value |
| `targetDisplayString` | body | `string` | no | The textual representation of the goal target |
| `trend` | body | `number` | no | The goal value trend |
| `value` | body | `number` | no | The goal current value |
| `valueDisplayString` | body | `string` | no | The textual representation of the current goal value |
