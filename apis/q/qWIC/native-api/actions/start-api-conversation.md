# Start API Conversation with QWIC

Starts a conversation in QWIC through the API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversations`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Start API Conversation](https://qwic-1.gitbook.io/help/deploying-agents/publishing-agents/api#start-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `object` | yes | Initial API conversation message object, typically a text message. |
| `variables` | body | `object` | yes | Conversation, contact, and system variables object. |
| `bot_key` | body | `string` | yes | Published bot key for an API-channel bot. |
| `from` | body | `object` | yes | Visitor origin object with user_external_id and type VISITOR. |
