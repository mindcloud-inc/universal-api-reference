# Create Team Activity Report with Timizer

Creates a team activity report in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/admin-teams/:teamId/activity-reports`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Team Activity Report](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `number` | yes | ID of the team. |
| `clientId` | body | `number` | yes | ID of the client. |
| `contractedId` | body | `number` | yes | ID of the contracted company. |
| `year` | body | `number` | yes | Target year. |
| `month` | body | `number` | yes | Target month. |
| `type` | body | `list` | no | Activity report type. Accepted values: `day`, `hour`. |
| `userId` | body | `number` | no | ID of the user that will own the activity report. |
| `missionId` | body | `number` | no | Optional mission ID. |
| `clientContactId` | body | `number` | no | Optional client contact ID. |
| `contractedContactId` | body | `number` | no | Optional contracted contact ID. |
| `rating` | body | `number` | no | Optional rating. |
| `note` | body | `string` | no | Optional activity report note. |
| `workDays[]` | body | `array<object>` | yes | Work day entries for the activity report. |
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
