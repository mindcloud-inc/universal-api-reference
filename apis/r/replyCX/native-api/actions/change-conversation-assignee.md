# Change Conversation Assignee with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Change Conversation Assignee](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes |
| `user.by` | body | `string` | yes |
| `user.to` | body | `string` | yes |
