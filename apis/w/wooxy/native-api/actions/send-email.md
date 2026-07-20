# Send Email with Wooxy

Sends an email through your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/mailer/send`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Send Email](https://wooxy.com/api-documentation/email/send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from.email` | body | `string` | yes | The sender email address on a verified Wooxy domain. |
| `from.name` | body | `string` | no | Optional sender display name. |
| `to.email` | body | `string` | yes | The recipient email address. |
| `to.name` | body | `string` | no | Optional recipient display name. |
| `subject` | body | `string` | yes | The message subject. |
| `html` | body | `string` | yes | The HTML body content. |
| `text` | body | `string` | no | Optional plain-text body content. |
