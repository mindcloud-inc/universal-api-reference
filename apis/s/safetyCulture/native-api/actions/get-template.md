# Get Template with SafetyCulture

Retrieves a template from SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/v1/templates/{template_id}`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Get Template](https://developer.safetyculture.com/reference/templatesservice_gettemplatebyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | Unique template id |
| `locale` | query | `string` | no | The preferred locale of the template. |
