# Send Email with Resend

Creates a new email in Resend.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Send Email](https://resend.com/docs/api-reference/emails/send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender email address. |
| `to` | body | `string` | yes | Recipient email address. |
| `subject` | body | `string` | yes | Email subject line. |
| `html` | body | `string` | no | HTML body of the email. |
| `scheduled_at` | body | `string` | no | When to send the email later. |
