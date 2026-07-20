# Get Template with Mailchimp

Retrieves a template from Mailchimp.

## Endpoint

- **Method:** `GET`
- **Path:** `templates/:template_id`
- **Base URL:** `https://{serverPrefix}.api.mailchimp.com/3.0/`
- **Official documentation:** [Get Template](https://us22.api.mailchimp.com/schema/3.0/Paths/Templates/Instance.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exclude_fields` | query | `string` | no | — |
| `fields` | query | `string` | no | — |
| `template_id` | path | `string` | yes | The unique ID for the template. |
