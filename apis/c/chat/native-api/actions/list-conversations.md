# List Conversations with 2Chat

Retrieves WhatsApp conversations from 2Chat for a channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/conversations/:channel_uuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List Conversations](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | path | `string` | yes | The UUID of the WhatsApp channel connected to 2Chat. |
| `page_number` | query | `number` | no | Zero-based page number for older conversation pages. |
| `phone_number` | query | `string` | no | Filter conversations by digits contained in the phone number. |
