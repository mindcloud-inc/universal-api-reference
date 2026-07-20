# Update Reminder with folk

Updates an existing reminder in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/reminders/:reminderId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Reminder](https://developer.folk.app/api-reference/reminders/update-a-reminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reminderId` | path | `string` | yes | The ID of the reminder to update. |
| `name` | body | `string` | no | The updated name of the reminder. |
| `recurrenceRule` | body | `string` | no | The updated reminder recurrence rule in the supported iCalendar subset. |
| `visibility` | body | `string` | no | The reminder visibility. Set public or private. |
| `assignedUsers[0].id` | body | `string` | no | The first assigned user ID when updating a public reminder. |
| `assignedUsers[0].email` | body | `string` | no | The first assigned user email when updating a public reminder. |
| `assignedUsers[1].id` | body | `string` | no | The second assigned user ID when updating a public reminder. |
| `assignedUsers[1].email` | body | `string` | no | The second assigned user email when updating a public reminder. |
