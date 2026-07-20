# Set Reminders with Amazing Marvin

Sets one or more reminders in Amazing Marvin.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminder/set`
- **Base URL:** `https://serv.amazingmarvin.com/api`
- **Official documentation:** [Set Reminders](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#set-reminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reminders[]` | body | `array<object>` | yes | Array of reminder objects to create or update. |
| `reminders[].time` | body | `number` | no | Unix timestamp for the reminder. |
| `reminders[].offset` | body | `number` | no | Minutes ahead of time to remind; use -1 for the Marvin default. |
| `reminders[].reminderId` | body | `string` | no | Unique reminder identifier, usually a task ID or random ID. |
| `reminders[].type` | body | `string` | no | Reminder type code such as T, M, DT, DP, or t. |
| `reminders[].title` | body | `string` | no | Reminder title shown in the notification. Maximum length: 200. |
| `reminders[].snooze` | body | `number` | no | Snooze duration in minutes. |
| `reminders[].autoSnooze` | body | `boolean` | no | Whether the reminder should auto-snooze. |
| `reminders[].canTrack` | body | `boolean` | no | Whether the reminder can start time tracking. |
