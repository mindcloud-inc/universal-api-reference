# List Reminders with Nozbe Teams

Retrieves accessible reminders from Nozbe Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/reminders`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Reminders](https://api4.nozbe.com/v1/api#/reminders/getReminders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | query | `string` | no | Return only reminders for this task. |
