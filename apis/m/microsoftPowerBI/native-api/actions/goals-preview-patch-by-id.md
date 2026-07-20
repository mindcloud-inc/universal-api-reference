# Patch By ID with Microsoft Power BI

## Endpoint

- **Method:** `PATCH`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Patch By ID](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/patch-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `goalId` | path | `string` | yes | The unique identifier of the goal |
| `aggregations[]` | body | `array<object>` | no | The list of aggregated properties of the goal |
| `completionDate` | body | `date` | no | The UTC timestamp for the completion date of the goal. The time portion of the timestamp is zero. |
| `createdTime` | body | `date` | no | The UTC time at creation |
| `datesFormatString` | body | `string` | no | datesFormatString |
| `description` | body | `string` | no | The goal description |
| `goalValues[]` | body | `array<object>` | no | The list of goal value check-ins |
| `hasStatusRules` | body | `boolean` | no | Whether the goal has status rules defined |
| `id` | body | `string` | no | The goal ID |
| `lastModifiedTime` | body | `date` | no | The UTC time at last modification |
| `level` | body | `number` | no | The nested level of the goal in the parent-child hierarchy of scorecard goals |
| `name` | body | `string` | no | The goal name |
| `notesCount` | body | `number` | no | notesCount |
| `parentId` | body | `string` | no | The ID of the parent goal, if defined. |
| `permissions` | body | `object` | no | The goal permissions |
| `rank` | body | `number` | no | The rank of the goal within the ordered set of sibling goals |
| `startDate` | body | `date` | no | The UTC timestamp for the start date of the goal. The time portion of the timestamp is zero. |
| `statusRules` | body | `object` | no | The goal status rules |
| `valuesFormatString` | body | `string` | no | valuesFormatString |
