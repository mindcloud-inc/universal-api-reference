# Get Chat History with Chatnode

## Endpoint

- **Method:** `POST`
- **Path:** `get-chats/:botId`
- **Base URL:** `https://api.public.chatnode.ai/v1`
- **Official documentation:** [Get Chat History](https://www.chatnode.ai/docs/developer-guides/api/get-chat-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The Chatnode agent id associated with the trained agent model. |
| `conversationSessionIds` | body | `string` | no | Conversation session ids to include in the raw JSON array request body documented by Chatnode. Send multiple values as a array. |
