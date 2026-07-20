# Send Email with MailerSend

## Endpoint

- **Method:** `POST`
- **Path:** `/email`
- **Base URL:** `https://api.mailersend.com/v1`
- **Official documentation:** [Send Email](https://developers.mailersend.com/api/v1/email#send-an-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from.email` | body | `string` | yes | Verified sender email address for this message. |
| `from.name` | body | `string` | no | Display name for the sender. |
| `html` | body | `string` | no | HTML body of the email. |
| `subject` | body | `string` | yes | Email subject line. |
| `text` | body | `string` | yes | Plain-text body of the email. |
| `to[].email` | body | `string` | yes | Email address for one recipient. |
| `to[].name` | body | `string` | no | Display name for one recipient. |
