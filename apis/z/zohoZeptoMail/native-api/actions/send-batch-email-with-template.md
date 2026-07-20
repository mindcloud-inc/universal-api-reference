# Send Batch Email with Template with Zoho ZeptoMail

Sends batch emails from a template in Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `email/template/batch`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Send Batch Email with Template](https://www.zoho.com/zeptomail/help/api/batch-email-templates.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_key` | body | `string` | yes | Template key to use when sending. |
| `from.address` | body | `string` | yes | Verified sender email address. |
| `to[].email_address.address` | body | `string` | yes | Recipient email address. |
