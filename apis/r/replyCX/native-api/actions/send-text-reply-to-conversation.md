# Send Text Reply To Conversation with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Send Text Reply To Conversation](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | — |
| `user.by` | body | `string` | yes | Email of the ReplyCX user sending the agent reply. |
| `message.data.body` | body | `string` | yes | Live ReplyCX contract for text replies. The public docs currently show `message.text`, but runtime accepts `message.data.body`. |
