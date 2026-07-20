# Update Template with Wooxy

Updates an existing template in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/template/email/update`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Update Template](https://wooxy.com/api-documentation/templates/update-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | The Wooxy template ID. |
| `name` | body | `string` | no | Optional updated template name. |
| `subject` | body | `string` | no | Optional updated email subject. |
| `html` | body | `string` | no | Optional updated HTML or text content. |
