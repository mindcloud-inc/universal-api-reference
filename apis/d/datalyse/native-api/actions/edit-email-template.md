# Edit Email Template with Datalyse

Updates an existing email template in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/emails/templates/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Email Template](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | Template HTML content (optional) |
| `name` | body | `string` | no | Template name (optional) |
| `subject` | body | `string` | no | Default email subject (optional) |
| `template_id` | body | `string` | yes | ID of the template to edit |
