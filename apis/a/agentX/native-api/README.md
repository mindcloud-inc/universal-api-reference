# AgentX: Native API Reference

A consolidated summary of AgentX's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.agentx.so/docs
- **API base URL:** `https://api.agentx.so/api/v1/access`

## Authentication

### API Key

Connect AgentX with an API key from your AgentX account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.agentx.so/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Conversation Context](actions/add-conversation-context.md) | `PUT /conversations/:id/update-context` | [docs](https://docs.agentx.so/reference/put_api-v1-access-conversations-id-update-context-1) |
| [Create Conversation](actions/create-conversation.md) | `POST /agents/:id/conversations/new` | [docs](https://docs.agentx.so/reference/post_api-v1-access-agents-id-conversations-new-1) |
| [Get Agent Detail](actions/get-agent-detail.md) | `GET /agents/:id` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-id-1) |
| [Get Conversation Detail](actions/get-conversation-detail.md) | `GET /agents/:id/conversations/:cid` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-id-conversations-cid-1) |
| [Get User Profile](actions/get-user-profile.md) | `GET /getProfile` | [docs](https://docs.agentx.so/reference/get_api-v1-access-getprofile-1) |
| [List Agents](actions/list-agents.md) | `GET /agents` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-1) |
| [List Agents As Object](actions/list-agents-as-object.md) | `GET /agents-obj` |  |
| [List Conversations](actions/list-conversations.md) | `GET /agents/:id/conversations` | [docs](https://docs.agentx.so/reference/get_api-v1-access-agents-id-conversations-1) |
| [Reset Conversation Context](actions/reset-conversation-context.md) | `DELETE /conversations/:id` | [docs](https://docs.agentx.so/reference/delete_api-v1-access-conversations-id-1) |
| [Send Message](actions/send-message.md) | `POST /conversations/:id/message` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-message-1) |
| [Send Message SSE](actions/send-message-sse.md) | `POST /conversations/:id/messagesse` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-messagesse-1) |
| [Send Message SSE With Stream](actions/send-message-sse-with-stream.md) | `POST /conversations/:id/jsonmessagesse` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-jsonmessagesse) |
| [Send Message With Attachment](actions/send-message-with-attachment.md) | `POST /conversations/:id/attachment` | [docs](https://docs.agentx.so/reference/post_api-v1-access-conversations-id-attachment-1) |
| [Vote On Message](actions/vote-on-message.md) | `PUT /vote/message/:id` |  |
