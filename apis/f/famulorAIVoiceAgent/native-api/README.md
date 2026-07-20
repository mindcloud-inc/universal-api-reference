# Famulor AI - Voice Agent: Native API Reference

A consolidated summary of Famulor AI - Voice Agent's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.famulor.io/en/api-reference/introduction.md
- **API base URL:** `https://app.famulor.de/api`

## Authentication

### API Key

Authenticate Famulor API requests with an API key in the Authorization Bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.famulor.io/en/api-reference/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Assistant](actions/create-assistant.md) | `POST /user/assistant` | [docs](https://docs.famulor.io/en/api-reference/assistants/create) |
| [Create Campaign](actions/create-campaign.md) | `POST /user/campaign` | [docs](https://docs.famulor.io/en/api-reference/campaigns/create) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://docs.famulor.io/en/api-reference/ai-chatbot/create-conversation) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /user/knowledgebases` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/create) |
| [Create Lead](actions/create-lead.md) | `POST /user/lead` | [docs](https://docs.famulor.io/en/api-reference/leads/create) |
| [Create Mid Call Tool](actions/create-mid-call-tool.md) | `POST /user/tools` | [docs](https://docs.famulor.io/en/api-reference/mid-call-tools/create-tool) |
| [Delete Assistant](actions/delete-assistant.md) | `DELETE /user/assistant/:id` | [docs](https://docs.famulor.io/en/api-reference/assistants/delete) |
| [Delete Call](actions/delete-call.md) | `DELETE /user/calls/:id` | [docs](https://docs.famulor.io/en/api-reference/calls/delete) |
| [Delete Knowledge Base](actions/delete-knowledge-base.md) | `DELETE /user/knowledgebases/:id` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/delete) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /user/leads/:id` | [docs](https://docs.famulor.io/en/api-reference/leads/delete) |
| [Delete Mid Call Tool](actions/delete-mid-call-tool.md) | `DELETE /user/tools/:id` | [docs](https://docs.famulor.io/en/api-reference/mid-call-tools/delete-tool) |
| [Disable Assistant Inbound Webhook](actions/disable-assistant-inbound-webhook.md) | `POST /user/assistants/disable-inbound-webhook` | [docs](https://docs.famulor.io/en/api-reference/assistants/disable-inbound-webhook) |
| [Disable Assistant Webhook](actions/disable-assistant-webhook.md) | `POST /user/assistants/disable-webhook` | [docs](https://docs.famulor.io/en/api-reference/assistants/disable-webhook) |
| [Enable Assistant Inbound Webhook](actions/enable-assistant-inbound-webhook.md) | `POST /user/assistants/enable-inbound-webhook` | [docs](https://docs.famulor.io/en/api-reference/assistants/enable-inbound-webhook) |
| [Generate AI Reply](actions/generate-ai-reply.md) | `POST /ai-replies/generate` | [docs](https://docs.famulor.io/en/api-reference/ai-replies/generate-reply) |
| [Get Call](actions/get-call.md) | `GET /user/calls/:id` | [docs](https://docs.famulor.io/en/api-reference/user/calls/get) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:uuid` | [docs](https://docs.famulor.io/en/api-reference/ai-chatbot/get-conversation) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /user/knowledgebases/:id` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/get) |
| [Get Knowledge Base Document](actions/get-knowledge-base-document.md) | `GET /user/knowledgebases/:knowledgebaseId/documents/:id` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/get-document) |
| [Get Mid Call Tool](actions/get-mid-call-tool.md) | `GET /user/tools/:id` | [docs](https://docs.famulor.io/en/api-reference/mid-call-tools/get-tool) |
| [Get Outbound Assistants](actions/get-outbound-assistants.md) | `GET /user/assistants/outbound` | [docs](https://docs.famulor.io/en/api-reference/assistants/outbound) |
| [Get User Information](actions/get-user-information.md) | `GET /user/me` | [docs](https://docs.famulor.io/en/api-reference/user/me) |
| [List Assistants](actions/list-assistants.md) | `GET /user/assistants/get` | [docs](https://docs.famulor.io/en/api-reference/assistants/list) |
| [List Calls](actions/list-calls.md) | `GET /user/calls` | [docs](https://docs.famulor.io/en/api-reference/calls/list) |
| [List Campaigns](actions/list-campaigns.md) | `GET /user/campaigns` | [docs](https://docs.famulor.io/en/api-reference/campaigns/list) |
| [List Knowledge Base Documents](actions/list-knowledge-base-documents.md) | `GET /user/knowledgebases/:knowledgebaseId/documents` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/list-documents) |
| [List Knowledge Bases](actions/list-knowledge-bases.md) | `GET /user/knowledgebases` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/list) |
| [List Leads](actions/list-leads.md) | `GET /user/leads` | [docs](https://docs.famulor.io/en/api-reference/leads/list) |
| [List Mid Call Tools](actions/list-mid-call-tools.md) | `GET /user/tools` | [docs](https://docs.famulor.io/en/api-reference/mid-call-tools/get-tools) |
| [Make a Call](actions/make-call.md) | `POST /user/make_call` | [docs](https://docs.famulor.io/en/api-reference/calls/make) |
| [Retrieve Available Languages](actions/retrieve-available-languages.md) | `GET /user/assistants/languages` | [docs](https://docs.famulor.io/en/api-reference/assistants/languages) |
| [Retrieve Available Models](actions/retrieve-available-models.md) | `GET /user/assistants/models` | [docs](https://docs.famulor.io/en/api-reference/assistants/models) |
| [Retrieve Available Phone Numbers](actions/retrieve-available-phone-numbers.md) | `GET /user/assistants/phone-numbers` | [docs](https://docs.famulor.io/en/api-reference/assistants/phone-numbers) |
| [Retrieve Available Voices](actions/retrieve-available-voices.md) | `GET /user/assistants/voices` | [docs](https://docs.famulor.io/en/api-reference/assistants/voices) |
| [Send Conversation Message](actions/send-conversation-message.md) | `POST /conversations/:uuid/messages` | [docs](https://docs.famulor.io/en/api-reference/ai-chatbot/send-conversation) |
| [Update Assistant](actions/update-assistant.md) | `PUT /user/assistant/:id` | [docs](https://docs.famulor.io/en/api-reference/assistants/update) |
| [Update Campaign Status](actions/update-campaign-status.md) | `POST /user/campaigns/update-status` | [docs](https://docs.famulor.io/en/api-reference/campaigns/update-status) |
| [Update Knowledge Base](actions/update-knowledge-base.md) | `PUT /user/knowledgebases/:id` | [docs](https://docs.famulor.io/en/api-reference/knowledgebases/update) |
| [Update Lead](actions/update-lead.md) | `PUT /user/leads/:id` | [docs](https://docs.famulor.io/en/api-reference/leads/update) |
| [Update Mid Call Tool](actions/update-mid-call-tool.md) | `PUT /user/tools/:id` | [docs](https://docs.famulor.io/en/api-reference/mid-call-tools/update-tool) |
