# Forward Email with Instantly

Forwards an email in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/emails/forward`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Forward Email](https://developer.instantly.ai/api-reference/email/forward-an-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reply_to_uuid` | body | `string` | yes | ID of the existing email to forward. |
| `eaccount` | body | `string` | yes | Connected email account used to forward the email. |
| `to_address_email_list` | body | `string` | yes | Comma-separated forward recipient email addresses. |
| `subject` | body | `string` | yes | Forward email subject. |
| `body` | body | `object` | yes | Forward email body object with html and/or text. |
