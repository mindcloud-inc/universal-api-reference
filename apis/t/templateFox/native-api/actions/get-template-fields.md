# Get Template Fields with TemplateFox

Retrieves template fields from TemplateFox.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/{{template_id}}/fields`
- **Base URL:** `https://api.templatefox.com`
- **Official documentation:** [Get Template Fields](https://templatefox.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | Template short ID (12 characters). |
