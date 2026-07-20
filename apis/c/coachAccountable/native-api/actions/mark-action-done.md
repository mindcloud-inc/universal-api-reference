# Mark Action Done with CoachAccountable

Marks an action done in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Mark Action Done](https://www.coachaccountable.com/APIDocs#Action.markDone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ActionID` | body | `number` | yes | — |
| `dateDone` | body | `date` | no | Optionally specify when the Action was completed, otherwise defaults to the time of the call. |
| `timeDone` | body | `string` | no | Optionally specify when the Action was completed, otherwise defaults to the time of the call. |
| `timezoneOf` | body | `list` | no | Who's timezone the date done is in. Defaults to that of the assigning Coach. Accepted values: `A`, `C`, `L`. |
| `comment` | body | `string` | no | Optional comment to be posted on the Action as part of completing it. Will show as written by the assigning coach (or the client's primary coach if client-assigned). |
