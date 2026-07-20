# Create SMS Conversation with QWIC

Creates an SMS conversation in QWIC.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/conversations`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Create SMS Conversation](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Configured SMS sender number. |
| `to` | body | `object` | yes | Recipient contact object with phone and optional name/email. |
| `message` | body | `object` | yes | SMS message object. QWIC docs show text payloads for this endpoint. |
| `assignee` | body | `string` | no | Optional agent email to assign the new conversation. |
