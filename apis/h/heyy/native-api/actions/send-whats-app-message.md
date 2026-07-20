# Send WhatsApp Message with Heyy

Sends a WhatsApp message from a Heyy channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/[:channelId]/whatsapp_messages/send`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Send WhatsApp Message](https://docs.heyy.io/api-reference/send-whatsapp-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The channel ID. |
| `fileId` | body | `string` | no | Optional uploaded file ID. |
| `messageTemplateId` | body | `string` | yes | The Heyy message template ID. |
| `phoneNumber` | body | `string` | yes | The destination phone number. |
| `scheduledAt` | body | `string` | no | Optional scheduled send time in ISO 8601 format. |
| `type` | body | `string` | yes | The WhatsApp message type. |
| `variables[]` | body | `array<object>` | no | Optional template variables. |
