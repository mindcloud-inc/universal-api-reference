# Send Contact with Chatvolt AI

Sends a contact message through Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/interactive/send-contact`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Send Contact](https://docs.chatvolt.ai/api-reference/endpoint/whatsapp/send-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `conversationId` | body | `string` | yes | The ID of the conversation. |
| `name_formatted_name` | body | `string` | yes | Full name as it should appear. |
