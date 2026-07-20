# Update Template with Zoho ZeptoMail

Updates an existing email template in Zoho ZeptoMail.

## Endpoint

- **Method:** `PUT`
- **Path:** `agents/:agentAlias/templates/:templateKey`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Update Template](https://www.zoho.com/zeptomail/help/api/update-template.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_alias` | body | `string` | no | Optional alias for the template. |
| `template_name` | body | `string` | yes | Name of the template. |
| `templateKey` | path | `string` | yes | Template key to update. |
| `subject` | body | `string` | yes | Template subject. |
| `htmlbody` | body | `string` | no | HTML template body. |
| `textbody` | body | `string` | no | Plain text template body. |
