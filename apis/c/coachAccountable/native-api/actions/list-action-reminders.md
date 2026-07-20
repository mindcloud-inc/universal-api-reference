# List Action Reminders with CoachAccountable

Retrieves action reminders from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Action Reminders](https://www.coachaccountable.com/APIDocs#Action.getReminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ActionID` | body | `number` | yes | — |
| `includeSent` | body | `boolean` | no | Set to true to include Reminders that have already been sent (otherwise just return future reminders, i.e. those yet to be sent. |
