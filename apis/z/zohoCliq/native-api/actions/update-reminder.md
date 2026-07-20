# Update Reminder with Zoho Cliq

Updates an existing reminder in Zoho Cliq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reminders/:reminderId`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Update Reminder](https://www.zoho.com/cliq/help/restapi/v2/#update_reminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reminderId` | path | `string` | yes | The ID of the reminder to update. |
| `content` | body | `string` | yes | The updated reminder content. |
| `time` | body | `number` | no | The updated reminder trigger time in milliseconds. |
