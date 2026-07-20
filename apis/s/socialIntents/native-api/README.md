# Social Intents: Native API Reference

A consolidated summary of Social Intents's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.socialintents.com/docs/integrations/rest-api-overview
- **API base URL:** `https://www.socialintents.com/v1/api`

## Authentication

### API Key

Connect with a Social Intents API token from Settings > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-SocialIntentsToken: <apiKey>
```

[Official authentication documentation](https://www.socialintents.com/docs/integrations/rest-api-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `apps`.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Completed Webhook](actions/create-chat-completed-webhook.md) | `POST /apps/:appId/webhook` | [docs](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts) |
| [Create Lead Captured Webhook](actions/create-lead-captured-webhook.md) | `POST /apps/:appId/webhook` | [docs](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts) |
| [Create Offline Message Webhook](actions/create-offline-message-webhook.md) | `POST /apps/:appId/webhook` | [docs](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhook/:webhookId` | [docs](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts) |
| [Delete Widget Webhook](actions/delete-widget-webhook.md) | `DELETE /apps/:appId/webhook/:webhookId` | [docs](https://www.socialintents.com/docs/integrations/webhooks-leads-transcripts) |
| [Get Chat By ID](actions/get-chat-by-id.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [Get Offline Message By ID](actions/get-offline-message-by-id.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats](actions/list-chats.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats By Date Range](actions/list-chats-by-date-range.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats By Email](actions/list-chats-by-email.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats By Timezone](actions/list-chats-by-timezone.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats By Visitor](actions/list-chats-by-visitor.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Chats By Widget](actions/list-chats-by-widget.md) | `GET /chats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Contacts By Date Range](actions/list-contacts-by-date-range.md) | `GET /contacts` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Contacts By Timezone](actions/list-contacts-by-timezone.md) | `GET /contacts` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Contacts By Widget](actions/list-contacts-by-widget.md) | `GET /contacts` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Contacts / Leads](actions/list-contacts-leads.md) | `GET /contacts` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats](actions/list-missed-chats.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats By Date Range](actions/list-missed-chats-by-date-range.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats By Email](actions/list-missed-chats-by-email.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats By Timezone](actions/list-missed-chats-by-timezone.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats By Visitor](actions/list-missed-chats-by-visitor.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Missed Chats By Widget](actions/list-missed-chats-by-widget.md) | `GET /missedchats` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages](actions/list-offline-messages.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages By Date Range](actions/list-offline-messages-by-date-range.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages By Email](actions/list-offline-messages-by-email.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages By Timezone](actions/list-offline-messages-by-timezone.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages By Visitor](actions/list-offline-messages-by-visitor.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Offline Messages By Widget](actions/list-offline-messages-by-widget.md) | `GET /offlinemessages` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [List Widgets](actions/list-widgets.md) | `GET /apps` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
| [Ping API](actions/ping-api.md) | `GET /ping` | [docs](https://www.socialintents.com/docs/integrations/rest-api-overview) |
