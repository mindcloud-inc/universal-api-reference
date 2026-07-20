# Send WhatsApp Message with Chatvolt AI

Sends a whatsApp Message through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapi/{instanceId}/{contactPhone}/message`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send WhatsApp Message](https://docs.chatvolt.ai/api-reference/endpoint/zapi/zapi-send-whatsapp-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instanceId` | path | `string` | yes | Z-API instance ID (externalId of the ServiceProvider of type 'zapi'). |
| `contactPhone` | path | `string` | yes | Recipient's WhatsApp number. |
| `message` | body | `string` | no | Textual content of the message. |
| `attachments[]` | body | `array<object>` | no | Optional list of attachments to be sent. |
