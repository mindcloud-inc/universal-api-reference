# Template API Request - Text with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/template-request`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Template API Request - Text](https://help.pickyassist.com/api-documentation-v2/whatsapp-template-api/template-request-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `message_type` | body | `number` | yes |
| `category` | body | `number` | yes |
| `messages[]` | body | `array<object>` | yes |
