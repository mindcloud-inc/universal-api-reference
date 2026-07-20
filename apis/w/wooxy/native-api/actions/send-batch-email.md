# Send Batch Email with Wooxy

Sends a batch email through Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/mailer/batch-send`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Send Batch Email](https://wooxy.com/api-documentation/email/send-batch-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from.email` | body | `string` | yes | The sender email address on a verified Wooxy domain. |
| `subject` | body | `string` | yes | The message subject. |
| `html` | body | `string` | yes | The HTML body content. |
| `recipients[]` | body | `array<object>` | yes | The recipient array, for example [{"email":"user@example.com"}]. |
