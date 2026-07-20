# AssignX: Native API Reference

A consolidated summary of AssignX's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://docs.agentx.so/reference
- **API base URL:** `https://api.agentx.so/api/v1/access/`

## Authentication

### API Key

Use the API key from the AgentX account panel. Requests must send the key in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.agentx.so/docs/getting-started)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Conversation](actions/create-conversation.md) | `POST agents/:id/conversations/new` | [docs](https://docs.agentx.so/reference/post_api-v1-access-agents-id-conversations-new-1) |
| [Get Conversation Detail](actions/get-conversation-detail.md) | `GET agents/:id/conversations/:cid` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-id-conversations-cid-1) |
| [Get Prompt Trace Detail](actions/get-prompt-trace-detail.md) | `GET traces/:id` | [docs](https://docs.agentx.so/reference/get_api-v1-access-traces-id-1) |
| [Get Prompt Trace for Message](actions/get-prompt-trace-for-message.md) | `GET messages/:id/trace` | [docs](https://docs.agentx.so/reference/get_api-v1-access-messages-id-trace-1) |
| [Get User Profile](actions/get-user-profile.md) | `GET getProfile` | [docs](https://docs.agentx.so/reference/get_api-v1-access-getprofile-1) |
| [List Agents](actions/list-agents.md) | `GET agents` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-1) |
| [List Conversations](actions/list-conversations.md) | `GET agents/:id/conversations` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-id-conversations-1) |
| [Reset Conversation Context](actions/reset-conversation-context.md) | `DELETE conversations/:id` | [docs](https://docs.agentx.so/reference/delete_api-v1-access-conversations-id-1) |
| [Send Message to Conversation](actions/send-message-to-conversation.md) | `POST conversations/:id/message` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-message-1) |
| [Send Message to Conversation (SSE)](actions/send-message-to-conversation-sse.md) | `POST conversations/:id/messagesse` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-messagesse-1) |
| [Send Message to Conversation (SSE) with Stream](actions/send-message-to-conversation-sse-with-stream.md) | `POST conversations/:id/jsonmessagesse` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-jsonmessagesse) |
| [Send Message to Conversation with Attachment](actions/send-message-to-conversation-with-attachment.md) | `POST conversations/:id/attachment` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-attachment-1) |
