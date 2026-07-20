# Create Reminder with folk

Creates a new reminder in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/reminders`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Reminder](https://developer.folk.app/api-reference/reminders/create-a-reminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity.id` | body | `string` | yes | The ID of the entity connected to the reminder. |
| `name` | body | `string` | yes | The name of the reminder. |
| `recurrenceRule` | body | `string` | yes | The reminder recurrence rule in the supported iCalendar subset. |
| `visibility` | body | `string` | yes | The reminder visibility. Defaulted to private in this action. |
| `assignedUsers[0].id` | body | `string` | no | The first assigned user ID for a public reminder. |
| `assignedUsers[0].email` | body | `string` | no | The first assigned user email for a public reminder. |
| `assignedUsers[1].id` | body | `string` | no | The second assigned user ID for a public reminder. |
| `assignedUsers[1].email` | body | `string` | no | The second assigned user email for a public reminder. |
