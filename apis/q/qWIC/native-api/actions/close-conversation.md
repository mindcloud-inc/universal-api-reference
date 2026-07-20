# Close Conversation with QWIC

Closes a QWIC conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Close Conversation](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#closing-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The QWIC conversation identifier. |
| `user.by` | body | `string` | yes | The agent email closing the conversation. |
