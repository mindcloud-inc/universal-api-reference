# Update Action with CoachAccountable

Updates an action in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Update Action](https://www.coachaccountable.com/APIDocs#Action.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ActionID` | body | `number` | yes | — |
| `theAction` | body | `string` | no | — |
| `dateDue` | body | `date` | no | — |
| `timeDue` | body | `string` | no | — |
| `timezoneOf` | body | `list` | no | Who's timezone the due date is in. Defaults to that of the assigning Coach. Accepted values: `A`, `C`, `L`. |
| `projectName` | body | `string` | no | Name of the Project for the Aaction to be filed under. If set to "NULL" the Action will be changed to a standalone one. |
| `ActionProjectID` | body | `number` | no | An alternative to projectName for specifying which project the Action should be filed under. |
| `weight` | body | `number` | no | Integer describing the relative significance of the Action within a project. Relevant only to Actions that are in a project. |
| `isLocked` | body | `boolean` | no | Prevent the Client from modifying or deleting the Action. |
