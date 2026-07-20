# Create WhatsApp Conversation with QWIC

Creates a WhatsApp conversation in QWIC.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Create WhatsApp Conversation](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Configured WhatsApp sender number. |
| `to` | body | `object` | yes | Recipient contact object with phone and optional name/email. |
| `message` | body | `object` | yes | WhatsApp message object. QWIC docs show template payloads for this endpoint. |
| `assignee` | body | `string` | no | Optional agent email to assign the new conversation. |
