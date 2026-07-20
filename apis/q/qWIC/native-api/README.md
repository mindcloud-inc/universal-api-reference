# QWIC: Native API Reference

A consolidated summary of QWIC's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis
- **API base URL:** `https://app.qwic.ai`

## Authentication

### API Key

Use a QWIC API key from Settings > Account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://qwic-1.gitbook.io/help/support-and-billing/user-management/inviting-teammates)

## API conventions

Responses from this API use JSON.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Knowledge Base Domain Data Source](actions/add-knowledge-base-domain-data-source.md) | `POST /v1/ai/knowledge-base/:knowledge_base_id/data-sources/domain` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-domain-data-source-to-a-knowledge-base) |
| [Add Knowledge Base Individual URL Data Sources](actions/add-knowledge-base-individual-url-data-sources.md) | `POST /v1/ai/knowledge-base/:knowledge_base_id/data-sources/webpages` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-individual-urls-data-sources-to-a-knowledge-base) |
| [Add Knowledge Base Text or File Data Sources](actions/add-knowledge-base-text-or-file-data-sources.md) | `POST /api/v1/ai/knowledge-base/:knowledge_base_id/upload/sources` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#adding-text-file-data-sources-to-a-knowledge-base) |
| [Close Conversation](actions/close-conversation.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#closing-a-conversation) |
| [Create Bot](actions/create-bot.md) | `POST /v1/bot` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#create-a-bot) |
| [Create Contacts](actions/create-contacts.md) | `POST /v1/conversations` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-contacts) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /v1/ai/knowledge-base` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#create-a-knowledge-base) |
| [Create SMS Conversation](actions/create-sms-conversation.md) | `POST /v1/conversations` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-a-conversation) |
| [Create WhatsApp Conversation](actions/create-whats-app-conversation.md) | `POST /v1/conversations` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#creating-a-conversation) |
| [Deploy Bot Flow](actions/deploy-bot-flow.md) | `POST /v1/bots/:bot_id/deploy` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#deploy-bot-flow) |
| [Fetch Bot Flow](actions/fetch-bot-flow.md) | `GET /v1/bots/:bot_id/flow` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-bot-flow) |
| [Fetch Knowledge Base Details](actions/fetch-knowledge-base-details.md) | `GET /v1/ai/knowledge-base/:knowledge_base_id` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-knowledge-base-details) |
| [Get Account Details](actions/get-account-details.md) | `GET /` |  |
| [Get Data Source Training Status](actions/get-data-source-training-status.md) | `GET /api/v1/ai/status/sources` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#get-training-status-of-a-data-source) |
| [List Bots](actions/list-bots.md) | `GET /v1/accounts/:account_id/bots` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-bots-list) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` |  |
| [Reassign Conversation To Agent](actions/reassign-conversation-to-agent.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#changing-assignee-in-a-conversation) |
| [Reassign Conversation To Team](actions/reassign-conversation-to-team.md) | `POST /api/v1/conversation/:conversation_id/events` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#changing-assignee-in-a-conversation) |
| [Send Agent Response to Conversation](actions/send-agent-response-to-conversation.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#send-agent-response-to-a-conversation) |
| [Send Visitor Response](actions/send-visitor-response.md) | `POST /api/v1/conversation/:conversation_id/messages` | [docs](https://qwic-1.gitbook.io/help/deploying-agents/publishing-agents/api#send-visitor-response) |
| [Set Events Webhook URL](actions/set-events-webhook-url.md) | `POST /v1/accounts/:account_id/webhook` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#set-webhook-url-for-events-feature) |
| [Start API Conversation](actions/start-api-conversation.md) | `POST /api/v1/conversations` | [docs](https://qwic-1.gitbook.io/help/deploying-agents/publishing-agents/api#start-conversation) |
| [Update Conversation Variables](actions/update-conversation-variables.md) | `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` | [docs](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#update-variable-of-a-conversation) |
