# List WhatsApp Templates with Landbot

Retrieves WhatsApp templates from Landbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/whatsapp/templates/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [List WhatsApp Templates](https://api.landbot.io/#api-WhatsApp_templates-GetHttpsApiLandbotIoV1ChannelsWhatsappTemplates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | query | `number` | no | Optional channel ID filter to avoid duplicate templates. |
