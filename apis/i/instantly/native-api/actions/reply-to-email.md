# Reply To Email with Instantly

Replies to an email in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/emails/reply`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Reply To Email](https://developer.instantly.ai/api-reference/email/reply-to-an-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reply_to_uuid` | body | `string` | yes | ID of the existing email to reply to. |
| `eaccount` | body | `string` | yes | Connected email account used to send the reply. |
| `subject` | body | `string` | yes | Email subject. |
| `body` | body | `object` | yes | Email body object with html and/or text. |
