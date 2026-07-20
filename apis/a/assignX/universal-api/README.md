# <img src="https://images.mindcloud.co/apps/icons/assign-x_1782739371713.png" alt="AssignX logo" width="28" height="28"> AssignX: Universal API

AssignX is an AI sales agent platform whose public API is still documented on the legacy AgentX domain. This app wraps the documented REST API for reading agents and managing agent conversations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assignX/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assignx.ai
- **Vendor API docs:** https://docs.agentx.so/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [List Agents](actions/list-agents.md) | GET | Retrieves agents you can access in AssignX. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in AssignX. |
| [Get Conversation Detail](actions/get-conversation-detail.md) | GET | Retrieves detailed conversation data from AssignX. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations for an AssignX agent. |
| [Reset Conversation Context](actions/reset-conversation-context.md) | DELETE | Resets stored conversation context in AssignX. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message to Conversation](actions/send-message-to-conversation.md) | POST | Sends a message in an AssignX conversation. |
| [Send Message to Conversation (SSE)](actions/send-message-to-conversation-sse.md) | POST | Sends a message and returns SSE events in AssignX. |
| [Send Message to Conversation (SSE) with Stream](actions/send-message-to-conversation-sse-with-stream.md) | POST | Sends a message and returns streamed JSON SSE events. |
| [Send Message to Conversation with Attachment](actions/send-message-to-conversation-with-attachment.md) | POST | Sends a message with an attachment in AssignX. |

### Trace

| Action | Method | Description |
| --- | --- | --- |
| [Get Prompt Trace Detail](actions/get-prompt-trace-detail.md) | GET | Retrieves prompt trace details from AssignX. |
| [Get Prompt Trace for Message](actions/get-prompt-trace-for-message.md) | GET | Retrieves a prompt trace for an AssignX message. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current user profile from AssignX. |

