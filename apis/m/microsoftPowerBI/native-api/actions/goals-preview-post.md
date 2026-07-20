# Post with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/scorecards([:scorecardId])/goals`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Post](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier of the workspace |
| `scorecardId` | path | `string` | yes | The unique identifier of the scorecard |
| `name` | body | `string` | yes | The goal name |
| `completionDate` | body | `date` | no | Optional. The UTC timestamp for the completion date of the goal. The time portion of the timestamp is zero. |
| `datesFormatString` | body | `string` | no | Optional. The custom format string for dates. |
| `parentId` | body | `string` | no | Optional. The ID of the parent goal, if defined. |
| `startDate` | body | `date` | no | Optional. The UTC timestamp for the start date of the goal. The time portion of the timestamp is zero. |
| `valuesFormatString` | body | `string` | no | Optional. The custom format string for values. |
