# Send Agent Response to Conversation with QWIC

Sends an agent response to a QWIC conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Send Agent Response to Conversation](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#send-agent-response-to-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID from Start API Conversation or another conversation-creation action. |
| `message` | body | `object` | yes | Agent text response payload from the QWIC public API docs. |
| `user.by` | body | `string` | yes | Agent email sending the response, as shown in the QWIC public API docs. |
