# Send Email with Zoho ZeptoMail

Sends a transactional email through Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `email`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Send Email](https://www.zoho.com/zeptomail/help/api/email-sending.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from.address` | body | `string` | yes | Verified sender email address for the selected ZeptoMail agent. |
| `from.name` | body | `string` | no | Sender display name. |
| `to[].email_address.address` | body | `string` | yes | Recipient email address. |
| `to[].email_address.name` | body | `string` | no | Recipient display name. |
| `subject` | body | `string` | yes | Email subject line. |
| `htmlbody` | body | `string` | no | HTML email body. ZeptoMail accepts either htmlbody or textbody. |
| `textbody` | body | `string` | no | Plain text email body. ZeptoMail accepts either textbody or htmlbody. |
| `track_clicks` | body | `boolean` | no | Enable ZeptoMail click tracking. |
| `track_opens` | body | `boolean` | no | Enable ZeptoMail open tracking. |
| `client_reference` | body | `string` | no | Client-defined identifier for the transaction. |
