# Create Chat Response with Vapi

Creates an OpenAI-compatible chat response in Vapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/responses`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Create Chat Response](https://docs.vapi.ai/api-reference/chats/create-response)

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
| `previousChatId` | body | `string` | no | This is the ID of the chat that will be used as context for the new chat. The messages from the previous chat will be used as context. Mutually exclusive with sessionId. |
| `transport` | body | `object` | no | — |
