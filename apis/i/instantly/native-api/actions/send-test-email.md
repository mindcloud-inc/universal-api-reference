# Send Test Email with Instantly

Sends a test email from Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/emails/test`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Send Test Email](https://developer.instantly.ai/api/v2/email/sendtestemail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eaccount` | body | `string` | yes | Connected email account used to send the test email. |
| `to_address_email_list` | body | `string` | yes | Comma-separated recipient email addresses. |
| `subject` | body | `string` | yes | Email subject. |
| `body` | body | `object` | yes | Email body object with html and/or text. |
