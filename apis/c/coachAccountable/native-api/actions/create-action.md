# Create Action with CoachAccountable

Creates an action in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Action](https://www.coachaccountable.com/APIDocs#Action.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | ID of the Client to whom this Action is to be assigned. |
| `theAction` | body | `string` | yes | A one-liner text of "what" the Action is. |
| `dateDue` | body | `date` | yes | Date on which the Action is to be done. |
| `timeDue` | body | `string` | yes | Time of day by which the Action is to be done. |
| `timezoneOf` | body | `list` | no | Who's timezone the due date is in. Defaults to that of the assigning Coach. Accepted values: `A`, `C`, `L`. |
| `comment` | body | `string` | no | An optional additional comment about this Action. |
| `sendNotification` | body | `boolean` | no | Send true to notify the client via email of this new Action. |
| `projectName` | body | `string` | no | Name of the Project for the new Action to be filed under. If left blank the new Action will be a standalone one. |
| `ActionProjectID` | body | `number` | no | An alternative to projectName for specifying which project the new Action should be filed under. |
| `weight` | body | `number` | no | Integer describing the relative significance of the Action within a project. Relevant only to Actions that are added to a project. |
| `isLocked` | body | `boolean` | no | Prevent the Client from modifying or deleting the Action. |
| `reminderSet` | body | `string` | no | A semi-colon-separated list of comma-separated triplets, each defining a reminder. In a triplet, the first value defines who to send it to ([C]oach or c[L]ient),the second value defines the send method ([E]mail or [T]ext), and the third value defines when to send the reminder, as minutes relative to the due date. |
