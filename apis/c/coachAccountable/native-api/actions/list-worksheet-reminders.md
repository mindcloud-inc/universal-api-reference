# List Worksheet Reminders with CoachAccountable

Retrieves worksheet reminders from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Worksheet Reminders](https://www.coachaccountable.com/APIDocs#Worksheet.getReminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WorksheetID` | body | `number` | yes | — |
| `includeSent` | body | `boolean` | no | Set to true to include Reminders that have already been sent (otherwise just return future reminders, i.e. those yet to be sent. |
