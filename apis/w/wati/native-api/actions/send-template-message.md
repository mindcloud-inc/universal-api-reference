# Send Template Message with Wati

Sends an approved WhatsApp template message through Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/sendTemplateMessage`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Send Template Message](https://docs.wati.io/reference/post_api-v1-sendtemplatemessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | query | `string` | yes | Target recipient phone number. |
| `template_name` | body | `string` | yes | Approved Wati template name. |
| `broadcast_name` | body | `string` | yes | Name for the broadcast record. |
| `parameters[]` | body | `array<object>` | no | Template parameter values for the message. |
