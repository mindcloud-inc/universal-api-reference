# Update Reminder with Vybit

## Endpoint

- **Method:** `PATCH`
- **Path:** `/vybit/{{key}}/reminders/{{reminderId}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Update Reminder](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cron` | body | `string` | no | Updated cron expression |
| `imageUrl` | body | `string` | no | Updated image URL |
| `key` | path | `string` | yes | The unique key of the vybit. |
| `linkUrl` | body | `string` | no | Updated link URL |
| `log` | body | `string` | no | Updated log content |
| `message` | body | `string` | no | Updated notification message |
| `reminderId` | path | `string` | yes | The unique ID of the reminder. |
| `timeZone` | body | `string` | no | Updated IANA time zone |
