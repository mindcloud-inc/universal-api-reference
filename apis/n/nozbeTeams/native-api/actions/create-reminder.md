# Create Reminder with Nozbe Teams

Creates a new reminder in Nozbe Teams.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminders`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Reminder](https://api4.nozbe.com/v1/api#/reminders/postReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | The task that will receive the reminder. |
| `remind_at` | body | `number` | yes | Unix timestamp in milliseconds for when to remind. |
| `is_relative` | body | `boolean` | yes | Whether the reminder is relative to the task date. |
| `is_all_day` | body | `boolean` | yes | Whether the reminder lasts all day. |
