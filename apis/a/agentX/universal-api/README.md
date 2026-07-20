# <img src="https://images.mindcloud.co/apps/icons/icon_1774536661150.png" alt="AgentX logo" width="28" height="28"> AgentX: Universal API

AgentX: Create, manage, and deploy AI agents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agentX/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.agentx.so/
- **Vendor API docs:** https://docs.agentx.so/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentX/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get Agent Detail](actions/get-agent-detail.md) | GET | Retrieves an agent's details from AgentX. |
| [List Agents](actions/list-agents.md) | GET | Retrieves a list of agents from AgentX. |
| [List Agents As Object](actions/list-agents-as-object.md) | GET | Retrieves agents as an object from AgentX. |

### Conversation Context

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversation Context](actions/add-conversation-context.md) | PUT | Updates conversation context in AgentX without triggering chat. |
| [Reset Conversation Context](actions/reset-conversation-context.md) | DELETE | Resets conversation context in AgentX. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | POST | Creates a new conversation in AgentX. |
| [Get Conversation Detail](actions/get-conversation-detail.md) | GET | Retrieves conversation details from AgentX. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves conversations for an agent from AgentX. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Message](actions/send-message.md) | POST | Sends a message to a conversation in AgentX. |
| [Send Message With Attachment](actions/send-message-with-attachment.md) | POST | Sends a message with an attachment in AgentX. |

### Message Stream

| Action | Method | Description |
| --- | --- | --- |
| [Send Message SSE](actions/send-message-sse.md) | POST | Sends a conversation message over SSE in AgentX. |
| [Send Message SSE With Stream](actions/send-message-sse-with-stream.md) | POST | Sends a conversation message with SSE streaming in AgentX. |

### Message Vote

| Action | Method | Description |
| --- | --- | --- |
| [Vote On Message](actions/vote-on-message.md) | PUT | Updates a message vote in AgentX. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current user profile from AgentX. |

