# Delete Action Project with CoachAccountable

Deletes an action project from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Delete Action Project](https://www.coachaccountable.com/APIDocs#Action.deleteProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `ActionProjectID` | body | `number` | yes | The ID of the Project you wish to delete. |
| `keepActions` | body | `boolean` | no | Keep Actions within a Project around as standalone Actions. If false, delete any Actions within the Project. |
