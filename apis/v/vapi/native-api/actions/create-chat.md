# Create Chat with Vapi

Creates a new chat in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Chat](https://docs.vapi.ai/api-reference/chats/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistantId` | body | `string` | no | This is the assistant that will be used for the chat. To use an existing assistant, use `assistantId` instead. |
| `assistant` | body | `object` | no | — |
| `assistantOverrides` | body | `object` | no | — |
| `squadId` | body | `string` | no | This is the squad that will be used for the chat. To use a transient squad, use `squad` instead. |
| `squad` | body | `object` | no | — |
| `name` | body | `string` | no | This is the name of the chat. This is just for your own reference. |
| `sessionId` | body | `string` | no | This is the ID of the session that will be used for the chat. Mutually exclusive with previousChatId. |
| `input` | body | `string` | yes | — |
| `stream` | body | `boolean` | no | This is a flag that determines whether the response should be streamed. When true, the response will be sent as chunks of text. |
| `previousChatId` | body | `string` | no | This is the ID of the chat that will be used as context for the new chat. The messages from the previous chat will be used as context. Mutually exclusive with sessionId. |
| `transport` | body | `object` | no | — |
