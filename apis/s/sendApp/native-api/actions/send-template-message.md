# Send Template Message with SendApp

## Endpoint

- **Method:** `GET`
- **Path:** `/send/template`
- **Base URL:** `https://official.sendapp.cloud/apiv3`
- **Official documentation:** [Send Template Message](https://official.sendapp.cloud/apiv3/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `button1` | query | `string` | no | Optional first button payload. |
| `button2` | query | `string` | no | Optional second button payload. |
| `button3` | query | `string` | no | Optional third button payload. |
| `header_media` | query | `string` | no | Optional header image or video URL. |
| `language_code` | query | `string` | yes | Template language code such as en, it, or es. |
| `number` | query | `string` | yes | WhatsApp number in international format with the + prefix. |
| `param1` | query | `string` | no | Optional first template parameter. |
| `param2` | query | `string` | no | Optional second template parameter. |
| `param3` | query | `string` | no | Optional third template parameter. |
| `template_id` | query | `string` | yes | Approved template ID. |
