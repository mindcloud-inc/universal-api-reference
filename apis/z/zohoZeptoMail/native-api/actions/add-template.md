# Add Template with Zoho ZeptoMail

Creates a new email template in Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `agents/:agentAlias/templates`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Add Template](https://www.zoho.com/zeptomail/help/api/add-template.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_name` | body | `string` | yes | Name of the template. |
| `template_alias` | body | `string` | no | Optional alias for the template. |
| `subject` | body | `string` | yes | Template subject. |
| `htmlbody` | body | `string` | no | HTML template body. |
| `textbody` | body | `string` | no | Plain text template body. |
