# WotNot: Native API Reference

A consolidated summary of WotNot's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.wotnot.io/build/integrations/public-apis
- **API base URL:** `https://api.wotnot.io`

## Authentication

### API Token

Use your WotNot account token from Settings > Account Settings > Developer.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.wotnot.io/build/integrations/public-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Knowledge Base Domain Source](actions/add-knowledge-base-domain-source.md) | `POST /v1/ai/knowledge-base/:knowledge_base_id/data-sources/domain` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Add Knowledge Base File Source](actions/add-knowledge-base-file-source.md) | `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Add Knowledge Base Text Source](actions/add-knowledge-base-text-source.md) | `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Add Knowledge Base Webpage Sources](actions/add-knowledge-base-webpage-sources.md) | `POST /v1/ai/knowledge-base/:knowledge_base_id/data-sources/webpages` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Change Conversation Assignee To Team](actions/change-conversation-assignee-to-team.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Change Conversation Assignee To User](actions/change-conversation-assignee-to-user.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Close Conversation](actions/close-conversation.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Create Bot](actions/create-bot.md) | `POST /v1/bot` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /v1/ai/knowledge-base` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Create Or Update Contact](actions/create-or-update-contact.md) | `POST /v1/conversations` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Delete Knowledge Base Data Sources](actions/delete-knowledge-base-data-sources.md) | `DELETE /v1/ai/knowledge-bases/:knowledge_base_id/data-sources` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Deploy Bot Flow](actions/deploy-bot-flow.md) | `POST /v1/bots/:bot_id/deploy` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Get Bot Flow](actions/get-bot-flow.md) | `GET /v1/bots/:bot_id/flow` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Get Knowledge Base Data Source Training Status](actions/get-knowledge-base-data-source-training-status.md) | `GET /api/v1/ai/status/sources` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Get Knowledge Base Details](actions/get-knowledge-base-details.md) | `GET /v1/ai/knowledge-base/:knowledge_base_id` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [List Bots](actions/list-bots.md) | `GET /v1/accounts/:account_id/bots` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Send Agent File Response](actions/send-agent-file-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Send Agent Template Response](actions/send-agent-template-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Send Agent Text Response](actions/send-agent-text-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Send Agent Voice Response](actions/send-agent-voice-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Send API Visitor Button Response](actions/send-api-visitor-button-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Send API Visitor File Upload Response](actions/send-api-visitor-file-upload-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Send API Visitor Multi-Button Response](actions/send-api-visitor-multi-button-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Send API Visitor Slider Response](actions/send-api-visitor-slider-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Send API Visitor Text Response](actions/send-api-visitor-text-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Set Events Webhook URL](actions/set-events-webhook-url.md) | `POST /v1/accounts/:account_id/webhook` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Start API Channel Conversation](actions/start-api-channel-conversation.md) | `POST /api/v1/conversations` | [docs](https://help.wotnot.io/deploy/publishing-agents/api) |
| [Start SMS Conversation](actions/start-sms-conversation.md) | `POST /api/v1/conversations` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Start WhatsApp Conversation](actions/start-whats-app-conversation.md) | `POST /api/v1/conversations` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
| [Update Conversation Variables](actions/update-conversation-variables.md) | `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` | [docs](https://help.wotnot.io/build/integrations/public-apis) |
