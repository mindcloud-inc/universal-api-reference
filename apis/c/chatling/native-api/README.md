# Chatling: Native API Reference

A consolidated summary of Chatling's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.chatling.ai/api-reference/v2/intro
- **API base URL:** `https://api.chatling.ai/v2`

## Authentication

### API Key

Authenticate with a Chatling API key as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.chatling.ai/api-reference/v2/introduction/api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `data.pages.last_page`. The current page number is read from `data.pages.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Chat With Knowledge Base AI](actions/chat-with-knowledge-base-ai.md) | `POST /chatbots/:chatbotId/ai/kb/chat` | [docs](https://docs.chatling.ai/api-reference/v2/ai-kb/chat) |
| [Create Contact](actions/create-contact.md) | `POST /chatbots/:chatbotId/contacts` | [docs](https://docs.chatling.ai/api-reference/v2/contacts/create-contact) |
| [Duplicate Chatbot](actions/duplicate-chatbot.md) | `POST /chatbots/:chatbotId/duplicate` | [docs](https://docs.chatling.ai/api-reference/v2/chatbots/duplicate-chatbot) |
| [Get AI Credits Usage](actions/get-ai-credits-usage.md) | `GET /usage/ai-credits` | [docs](https://docs.chatling.ai/api-reference/v2/usage/ai-credits) |
| [Get Chatbots Usage](actions/get-chatbots-usage.md) | `GET /usage/chatbots` | [docs](https://docs.chatling.ai/api-reference/v2/usage/chatbots) |
| [Get Email Credits Usage](actions/get-email-credits-usage.md) | `GET /usage/email-credits` | [docs](https://docs.chatling.ai/api-reference/v2/usage/email-credits) |
| [Get Knowledge Base Usage](actions/get-knowledge-base-usage.md) | `GET /usage/knowledge-base` | [docs](https://docs.chatling.ai/api-reference/v2/usage/knowledge-base) |
| [Get User Seats Usage](actions/get-user-seats-usage.md) | `GET /usage/user-seats` | [docs](https://docs.chatling.ai/api-reference/v2/usage/user-seats) |
| [List AI Languages](actions/list-ai-languages.md) | `GET /chatbots/:chatbotId/ai/kb/languages` | [docs](https://docs.chatling.ai/api-reference/v2/ai-kb/list-ai-languages) |
| [List AI Models](actions/list-ai-models.md) | `GET /chatbots/:chatbotId/ai/kb/models` | [docs](https://docs.chatling.ai/api-reference/v2/ai-kb/list-ai-models) |
| [List Chatbot Templates](actions/list-chatbot-templates.md) | `GET /chatbot-templates` | [docs](https://docs.chatling.ai/api-reference/v2/chatbots/list-chatbot-templates) |
| [List Chatbots](actions/list-chatbots.md) | `GET /chatbots` | [docs](https://docs.chatling.ai/api-reference/v2/chatbots/list-chatbots) |
| [List Contacts](actions/list-contacts.md) | `GET /chatbots/:chatbotId/contacts` | [docs](https://docs.chatling.ai/api-reference/v2/contacts/list-contacts) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /chatbots/:chatbotId/conversations/:conversationId/messages` | [docs](https://docs.chatling.ai/api-reference/v2/conversations/list-conversation-messages) |
| [List Conversations](actions/list-conversations.md) | `GET /chatbots/:chatbotId/conversations` | [docs](https://docs.chatling.ai/api-reference/v2/conversations/list-conversations) |
| [List Settings](actions/list-settings.md) | `GET /project/settings` | [docs](https://docs.chatling.ai/api-reference/v2/project/list-settings) |
| [Rate AI Answer](actions/rate-ai-answer.md) | `PATCH /chatbots/:chatbotId/conversations/:conversationId/messages/:messageId/rate-ai-answer` | [docs](https://docs.chatling.ai/api-reference/v2/conversations/rate-ai-answer) |
| [Retrieve Chatbot](actions/retrieve-chatbot.md) | `GET /chatbots/:chatbotId` | [docs](https://docs.chatling.ai/api-reference/v2/chatbots/retrieve-chatbot) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /chatbots/:chatbotId/contacts/:contactId` | [docs](https://docs.chatling.ai/api-reference/v2/contacts/retrieve-contact) |
| [Retrieve Conversation](actions/retrieve-conversation.md) | `GET /chatbots/:chatbotId/conversations/:conversationId` | [docs](https://docs.chatling.ai/api-reference/v2/conversations/retrieve-conversation) |
| [Update Chatbot Settings](actions/update-chatbot-settings.md) | `PATCH /chatbots/:chatbotId` | [docs](https://docs.chatling.ai/api-reference/v2/chatbots/update-chatbot-settings) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /chatbots/:chatbotId/conversations/:conversationId` | [docs](https://docs.chatling.ai/api-reference/v2/conversations/update-conversation) |
| [Update Settings](actions/update-settings.md) | `PATCH /project/settings` | [docs](https://docs.chatling.ai/api-reference/v2/project/update-settings) |
