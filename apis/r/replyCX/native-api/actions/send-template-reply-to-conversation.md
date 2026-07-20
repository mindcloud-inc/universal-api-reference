# Send Template Reply To Conversation with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Send Template Reply To Conversation](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes |
| `user.by` | body | `string` | yes |
| `message.data.template` | body | `string` | yes |
