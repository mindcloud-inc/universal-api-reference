# Schedule Sending Viber Messages with SMS.to

Schedules personalized Viber messages for later delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Schedule Sending Viber Messages](https://developers.sms.to/#c8047d14-7907-4207-b61d-57b284609df2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | body | `string` | yes | Each message text. |
| `messages[].to` | body | `string` | yes | Recipient phone number. |
| `scheduled_for` | body | `date` | no | Date and time when the messages will be sent. Format: YYYY-MM-DD HH:MM:SS. |
| `timezone` | body | `string` | no | TZ database name. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
