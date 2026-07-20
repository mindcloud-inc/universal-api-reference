# Update Team Activity Report with Timizer

Updates an existing team activity report in Timizer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/app/admin-teams/:teamId/activity-reports/:activityReportId`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Update Team Activity Report](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | ID of the team. |
| `activityReportId` | path | `number` | yes | ID of the activity report. |
| `clientId` | body | `number` | no | ID of the client. |
| `contractedId` | body | `number` | no | ID of the contracted company. |
| `year` | body | `number` | no | Target year. |
| `month` | body | `number` | no | Target month. |
| `type` | body | `list` | no | Activity report type. Accepted values: `day`, `hour`. |
| `missionId` | body | `number` | no | Optional mission ID. |
| `clientContactId` | body | `number` | no | Optional client contact ID. |
| `contractedContactId` | body | `number` | no | Optional contracted contact ID. |
| `rating` | body | `number` | no | Optional rating. |
| `note` | body | `string` | no | Optional activity report note. |
| `workDays[]` | body | `array<object>` | no | Work day entries for the activity report. |
| `workDays[].dayOfMonth` | body | `number` | no | Day of month for the work entry. |
| `workDays[].workedTime` | body | `list` | no | Worked time enum for the work entry. Accepted values: `custom`, `full`, `half`, `none`. |
| `workDays[].workedSeconds` | body | `number` | no | Worked seconds for custom time entries. |
| `workDays[].note` | body | `string` | no | Optional note for the work entry. |
| `workDays[].tags[]` | body | `array<object>` | no | Optional tags for the work entry. |
| `workDays[].tags[].id` | body | `number` | no | Optional tag ID. |
| `workDays[].tags[].label` | body | `string` | no | Tag label. |
| `workDays[].tags[].customId` | body | `string` | no | Optional tag custom ID. |
| `workDays[].tags[].textColor` | body | `string` | no | Optional tag text color. |
| `workDays[].tags[].backgroundColor` | body | `string` | no | Optional tag background color. |
| `workDays[].tags[].weight` | body | `number` | no | Optional tag weight. |
| `workDays[].tags[].workable` | body | `boolean` | no | Whether the tag is workable. |
| `workDays[].tags[].pricePerUnit` | body | `number` | no | Optional tag price per unit. |
| `workDays[].tags[].costPerUnit` | body | `number` | no | Optional tag cost per unit. |
