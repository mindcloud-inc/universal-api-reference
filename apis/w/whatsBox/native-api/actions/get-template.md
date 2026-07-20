# Get Template with WhatsBox

Retrieves a WhatsApp template from WhatsBox.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [Get Template](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template ID. |
| `type` | query | `string` | no | Template type. |
| `name` | query | `string` | no | Template name. |
