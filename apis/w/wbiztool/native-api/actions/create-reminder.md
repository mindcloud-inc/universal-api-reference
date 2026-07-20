# Create Reminder with Wbiztool

Creates a recurring WhatsApp reminder in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/reminder/create/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Create Reminder](https://wbiztool.com/docs/reminder-create-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg_type` | body | `string` | yes | Reminder message type as numeric text: 0 text, 1 image, 2 file. |
| `reminder_name` | body | `string` | yes | Friendly name for the reminder. |
| `phone` | body | `string` | yes | Recipient phone number, including country code. |
| `message` | body | `string` | yes | Reminder message text. |
| `cron_expression` | body | `string` | yes | Cron expression that defines when the reminder runs. |
| `timezone` | body | `string` | yes | Timezone used for the cron schedule. |
| `img_url` | body | `string` | no | Public image URL for image reminders. |
| `file_url` | body | `string` | no | Public file URL for file reminders. |
| `file_name` | body | `string` | no | Optional display name for file reminders. |
