# ReplyCX: Native API Reference

A consolidated summary of ReplyCX's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://help.reply.cx/integrations/public-apis
- **API base URL:** `https://api.reply.cx`

## Authentication

### API Key

Authenticate with a ReplyCX bearer token and account ID.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · The numeric ReplyCX account ID used in account-scoped endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.reply.cx/integrations/public-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `bots`.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Conversation Assignee](actions/change-conversation-assignee.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Close Conversation](actions/close-conversation.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Create Conversation](actions/create-conversation.md) | `POST /api/v1/conversations` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Get Data Source Training Status](actions/get-data-source-training-status.md) | `GET /api/v1/ai/status/sources` | [docs](https://help.reply.cx/integrations/public-apis) |
| [List Bots](actions/list-bots.md) | `GET /v1/accounts/:account_id/bots` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Send File Reply To Conversation](actions/send-file-reply-to-conversation.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Send Template Reply To Conversation](actions/send-template-reply-to-conversation.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Send Text Reply To Conversation](actions/send-text-reply-to-conversation.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Send Voice Reply To Conversation](actions/send-voice-reply-to-conversation.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Set Events Webhook](actions/set-events-webhook.md) | `POST /v1/accounts/:account_id/webhook` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Update Conversation Variables](actions/update-conversation-variables.md) | `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Upload Knowledge Base File Source](actions/upload-knowledge-base-file-source.md) | `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` | [docs](https://help.reply.cx/integrations/public-apis) |
| [Upload Knowledge Base Text Source](actions/upload-knowledge-base-text-source.md) | `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` | [docs](https://help.reply.cx/integrations/public-apis) |
