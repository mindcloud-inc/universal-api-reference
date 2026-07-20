# Delete Reminder with Vybit

## Endpoint

- **Method:** `DELETE`
- **Path:** `/vybit/{{key}}/reminders/{{reminderId}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Delete Reminder](https://developer.vybit.net/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | no | The unique key of the vybit. |
| `reminderId` | path | `string` | no | The unique ID of the reminder. |
