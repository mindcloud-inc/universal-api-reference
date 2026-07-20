# Set Self Reminder with Zoho Cliq

Creates a self reminder in Zoho Cliq.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminders`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Set Self Reminder](https://www.zoho.com/cliq/help/restapi/v2/#create_reminder_self)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The reminder content. |
| `time` | body | `number` | no | The reminder trigger time in milliseconds. |
