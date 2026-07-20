# Set Worksheet Reminders with CoachAccountable

Updates worksheet reminders in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Set Worksheet Reminders](https://www.coachaccountable.com/APIDocs#Worksheet.setReminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `WorksheetID` | body | `number` | yes | — |
| `reminderSet` | body | `string` | no | A semi-colon-separated list of comma-separated triplets, each defining a reminder. In a triplet, the first value defines who to send it to ([C]oach or c[L]ient),the second value defines the send method ([E]mail or [T]ext), and the third value defines when to send the reminder, as minutes relative to the due date. |
