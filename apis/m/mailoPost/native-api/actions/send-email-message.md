# Send Email Message with MailoPost

Sends an email message in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/messages`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Send Email Message](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_email` | body | `string` | yes | Sender email address. |
| `from_name` | body | `string` | no | Sender display name. |
| `to` | body | `string` | yes | Recipient email address. |
| `subject` | body | `string` | yes | Email subject line. |
| `text` | body | `string` | no | Plain-text message body. Provide text or html. |
| `html` | body | `string` | no | HTML message body. Provide html or text. |
| `payment` | body | `string` | no | Billing mode for the message. |
| `smtp_headers` | body | `object` | no | Additional SMTP headers. |
