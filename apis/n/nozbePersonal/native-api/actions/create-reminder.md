# Create Reminder with Nozbe Personal

Creates a new reminder in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminders`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Reminder](https://api4.nozbe.com/v1/api#/reminders/postReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | yes | Reminder task ID. |
| `remind_at` | body | `number` | yes | Reminder timestamp in milliseconds. |
| `is_relative` | body | `boolean` | yes | Whether the reminder is relative. |
| `is_all_day` | body | `boolean` | yes | Whether the reminder lasts all day. |
