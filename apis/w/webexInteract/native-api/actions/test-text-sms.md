# Test text SMS with Webex Interact

Tests an SMS message in Webex Interact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sms/test`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Test text SMS](https://docs.webexinteract.com/reference/sms-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `global_merge_fields` | body | `object` | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `message_body` | body | `string` | yes | SMS message content. Required unless template ID is provided. |
| `name` | body | `string` | no | External request name returned in webhooks. |
| `from` | body | `string` | yes | Sender ID for the SMS message. |
| `to` | body | `list<object>` | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |
| `skip_optout_check` | body | `boolean` | no | Bypass opt-out checks when true. |
