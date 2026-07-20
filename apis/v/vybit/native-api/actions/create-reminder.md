# Create Reminder with Vybit

## Endpoint

- **Method:** `POST`
- **Path:** `/vybit/{{key}}/reminders`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Create Reminder](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron` | body | `string` | yes | Cron expression for when the reminder should fire |
| `imageUrl` | body | `string` | no | Image URL for this reminder |
| `key` | path | `string` | yes | The unique key of the vybit. |
| `linkUrl` | body | `string` | no | Link URL for this reminder |
| `log` | body | `string` | no | Log content for this reminder |
| `message` | body | `string` | no | Notification message for this reminder |
| `timeZone` | body | `string` | no | IANA time zone identifier |
| `year` | body | `number` | no | Year for a one-time reminder |
