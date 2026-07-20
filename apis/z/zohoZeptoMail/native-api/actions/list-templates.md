# List Templates with Zoho ZeptoMail

Retrieves email templates from Zoho ZeptoMail.

## Endpoint

- **Method:** `GET`
- **Path:** `agents/:agentAlias/templates`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [List Templates](https://www.zoho.com/zeptomail/help/api/list-template.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of templates to return. |
| `offset` | query | `number` | no | Offset of the first template to return. |
