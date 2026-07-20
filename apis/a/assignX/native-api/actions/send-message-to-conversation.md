# Send Message to Conversation with AssignX

Sends a message in an AssignX conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `conversations/:id/message`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Send Message to Conversation](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-message-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Conversation identifier from List Agent Conversations or Create New Conversation. |
| `message` | body | `string` | yes | Message text to send to the conversation. |
