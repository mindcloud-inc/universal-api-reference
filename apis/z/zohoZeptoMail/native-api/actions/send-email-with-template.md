# Send Email with Template with Zoho ZeptoMail

Sends an email from a template in Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `email/template`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Send Email with Template](https://www.zoho.com/zeptomail/help/api/email-templates.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_key` | body | `string` | yes | Template key to use when sending. |
| `from.address` | body | `string` | yes | Verified sender email address. |
| `to[].email_address.address` | body | `string` | yes | Recipient email address. |
