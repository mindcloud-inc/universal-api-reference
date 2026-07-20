# Register Message in Context with Chatvolt AI

Registers a message in conversation context in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/message-register`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Register Message in Context](https://docs.chatvolt.ai/api-reference/endpoint/conversation/message-register)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation where the message will be registered. |
| `message` | body | `string` | yes | Text of the message to be registered. |
| `from` | body | `string` | no | Indicates the sender of the message. |
