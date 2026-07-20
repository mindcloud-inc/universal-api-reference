# List Actions with CoachAccountable

Retrieves actions from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Actions](https://www.coachaccountable.com/APIDocs#Action.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | Filter Actions by Client. |
| `ActionProjectID` | body | `number` | no | Filter the Actions you get back down to a given project. |
| `projectName` | body | `string` | no | Filter the Actions you get back by project name. Supports partial matches on prefix. |
| `includeDone` | body | `boolean` | no | Set to true to include Actions that have already been marked complete. |
| `includeCanceled` | body | `boolean` | no | Set to true to include Actions that have been canceled. |
| `includeForCoach` | body | `boolean` | no | Set to true to include Actions that are for the coach to do. |
