# Complete Reminder with Zoho Cliq

Marks a Zoho Cliq reminder as complete.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reminders/:reminderId/complete`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Complete Reminder](https://www.zoho.com/cliq/help/restapi/v2/#mark_reminder_complete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reminderId` | path | `string` | yes | The ID of the reminder to mark as complete. |
