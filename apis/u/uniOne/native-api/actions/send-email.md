# Send Email with UniOne

Sends an email message through UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `email/send.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Send Email](https://docs.unione.io/en/web-api-ref#email-send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.recipients[].email` | body | `string` | yes | Recipient email address. |
| `message.subject` | body | `string` | yes | Email subject. |
| `message.body.html` | body | `string` | yes | HTML body content. |
| `message.body.plaintext` | body | `string` | no | Plaintext fallback body. |
| `message.from_email` | body | `string` | yes | Sender email address. |
| `message.from_name` | body | `string` | yes | Sender name. |
