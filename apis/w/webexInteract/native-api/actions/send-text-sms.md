# Send text SMS with Webex Interact

Sends an SMS message from Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sms`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Send text SMS](https://docs.webexinteract.com/reference/sms-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `global_merge_fields` | body | `object` | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `message_body` | body | `string` | yes | SMS message content. Required unless template ID is provided. |
| `name` | body | `string` | no | External request name returned in webhooks. |
| `schedule_at` | body | `string` | no | Future ISO 8601 date/time for scheduled sending. |
| `valid_until` | body | `string` | no | ISO 8601 expiry time for delivery validity. |
| `from` | body | `string` | yes | Sender ID for the SMS message. Sender names must already exist in Webex Interact. |
| `to` | body | `list<object>` | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |
| `skip_optout_check` | body | `boolean` | no | Bypass opt-out checks when true. |
