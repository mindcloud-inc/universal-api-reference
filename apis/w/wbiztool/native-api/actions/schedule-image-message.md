# Schedule Image Message with Wbiztool

Creates a scheduled WhatsApp image message in Wbiztool.

## Endpoint

- **Method:** `POST`
- **Path:** `/schedule_msg/`
- **Base URL:** `https://wbiztool.com/api/v1`
- **Official documentation:** [Schedule Image Message](https://wbiztool.com/docs/schedule-message-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | no | Recipient phone number with or without country code. |
| `group_name` | body | `string` | no | WhatsApp group name to message instead of a direct phone number. |
| `country_code` | body | `string` | no | Country code for the recipient phone number. |
| `img_url` | body | `string` | yes | Public image URL to include with the message. |
| `msg` | body | `string` | yes | Caption text to schedule with the image. |
| `date` | body | `string` | yes | Date to send the message in dd/mm/yyyy format. |
| `time` | body | `string` | yes | Time to send the message in HH:MM format. |
| `timezone` | body | `string` | yes | Timezone used for the scheduled date and time. |
| `webhook` | body | `string` | no | Optional webhook URL to receive message events. |
| `expire_after_seconds` | body | `number` | no | Expire the message if it has not been sent before this many seconds. |
