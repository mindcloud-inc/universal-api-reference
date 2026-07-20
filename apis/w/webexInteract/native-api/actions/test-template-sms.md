# Test template SMS with Webex Interact

Tests a template SMS in Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sms/test`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Test template SMS](https://docs.webexinteract.com/reference/sms-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender ID for the SMS message. Sender names must already exist in Webex Interact. |
| `global_merge_fields` | body | `object` | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `name` | body | `string` | no | External request name returned in webhooks. |
| `skip_optout_check` | body | `boolean` | no | Bypass opt-out checks when true. |
| `template_id` | body | `string` | yes | Template ID from Webex Interact. Required for template SMS validation. |
| `to` | body | `list<object>` | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |
