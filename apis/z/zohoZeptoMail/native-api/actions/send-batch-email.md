# Send Batch Email with Zoho ZeptoMail

Sends transactional emails in bulk through Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `email/batch`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Send Batch Email](https://www.zoho.com/zeptomail/help/api/batch-email-sending.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from.address` | body | `string` | yes | Verified sender email address. |
| `to[].email_address.address` | body | `string` | yes | Recipient email address. |
| `subject` | body | `string` | yes | Email subject line. |
| `htmlbody` | body | `string` | no | HTML email body. |
