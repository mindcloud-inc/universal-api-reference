# Send File Reply To Conversation with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Send File Reply To Conversation](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes |
| `user.by` | body | `string` | yes |
| `message.file.path` | body | `string` | yes |
| `message.file.size` | body | `number` | yes |
| `message.file.type` | body | `string` | yes |
| `message.file.name` | body | `string` | yes |
