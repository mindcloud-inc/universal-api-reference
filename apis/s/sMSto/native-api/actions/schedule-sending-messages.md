# Schedule Sending Messages with SMS.to

Schedules personalized SMS messages for later delivery in SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Schedule Sending Messages](https://developers.sms.to/#32162af7-26e0-485a-87a4-d94ab6cdd1ba)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | body | `string` | yes | Each message text. |
| `messages[].to` | body | `string` | yes | Recipient phone number. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `scheduled_for` | body | `date` | no | Date and time when the messages will be sent. Format: YYYY-MM-DD HH:MM:SS. |
| `timezone` | body | `string` | no | TZ database name. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
