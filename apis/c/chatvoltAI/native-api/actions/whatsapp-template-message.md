# WhatsApp Template Message with Chatvolt AI

Sends a WhatsApp template message through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/{phoneNumberId}/template-message`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [WhatsApp Template Message](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/template-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumberId` | path | `string` | yes | ID of the WhatsApp Business phone number |
| `to` | body | `string` | yes | Recipient's phone number with country code |
| `text` | body | `string` | yes | Message text to store in conversation history |
| `agentId` | body | `string` | yes | ID of the agent to associate with this message |
| `templateName` | body | `string` | yes | Name of the pre-approved WhatsApp template |
| `templateLangCode` | body | `string` | yes | Language code for the template |
| `defaultStatus` | body | `string` | no | The default status to set for the conversation. |
| `buttons[]` | body | `array<object>` | no | Array of buttons for the template. |
