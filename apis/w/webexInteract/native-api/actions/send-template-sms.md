# Send template SMS with Webex Interact

Sends a template SMS from Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sms`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Send template SMS](https://docs.webexinteract.com/reference/sms-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender ID for the SMS message. Sender names must already exist in Webex Interact. |
| `global_merge_fields` | body | `object` | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `name` | body | `string` | no | External request name returned in webhooks. |
| `schedule_at` | body | `string` | no | Future ISO 8601 date/time for scheduled sending. |
| `skip_optout_check` | body | `boolean` | no | Bypass opt-out checks when true. |
| `template_id` | body | `string` | yes | Template ID from Webex Interact. Required for template SMS. |
| `to` | body | `list<object>` | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |
| `valid_until` | body | `string` | no | ISO 8601 expiry time for delivery validity. |
