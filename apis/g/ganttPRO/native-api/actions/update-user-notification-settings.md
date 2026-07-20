# Update User Notification Settings with GanttPRO

Updates notification settings for a GanttPRO user.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:userId/notification`
- **Base URL:** `https://api.ganttpro.com/v1.0`
- **Official documentation:** [Update User Notification Settings](https://developer.ganttpro.com/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | GanttPRO user identifier. |
| `envType` | body | `string` | yes | Notification channel: email, desktop, or mobile. Accepted values: `0`, `1`, `2`. |
| `actionType` | body | `string` | yes | Notification event type such as mention, assign, comment, attachment, task_start, deadline, team_invite, or task_end. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `active` | body | `number` | yes | Use 1 to enable the notification or 0 to disable it. Accepted values: `0`, `1`. |
