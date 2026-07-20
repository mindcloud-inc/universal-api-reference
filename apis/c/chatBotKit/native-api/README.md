# ChatBotKit: Native API Reference

A consolidated summary of ChatBotKit's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://chatbotkit.com/manuals/api
- **OpenAPI specification:** https://api.chatbotkit.com/v1/spec.json
- **API base URL:** `https://api.chatbotkit.com/v1`

## Authentication

### API Key

Authenticate ChatBotKit with a long-lived API secret key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://chatbotkit.com/manuals/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/plain, */*` |

Responses from this API use JSON. Response data is read from `items`. The next-page cursor is read from `cursor`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Conversation Interaction](actions/complete-conversation-interaction.md) | `POST /conversation/complete` | [docs](https://chatbotkit.com/manuals/conversation-flow) |
| [Create Bot](actions/create-bot.md) | `POST /bot/create` | [docs](https://chatbotkit.com/manuals/bots) |
| [Create Bot Session](actions/create-bot-session.md) | `POST /bot/{botId}/session/create` | [docs](https://chatbotkit.com/manuals/bot-sessions) |
| [Create Contact](actions/create-contact.md) | `POST /contact/create` | [docs](https://chatbotkit.com/manuals/contacts) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversation/create` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Create Conversation Message](actions/create-conversation-message.md) | `POST /conversation/{conversationId}/message/create` | [docs](https://chatbotkit.com/manuals/conversation-messages) |
| [Create Dataset](actions/create-dataset.md) | `POST /dataset/create` | [docs](https://chatbotkit.com/manuals/datasets) |
| [Create Dataset Record](actions/create-dataset-record.md) | `POST /dataset/{datasetId}/record/create` | [docs](https://chatbotkit.com/manuals/dataset-records) |
| [Delete Bot](actions/delete-bot.md) | `POST /bot/{botId}/delete` | [docs](https://chatbotkit.com/manuals/bots) |
| [Delete Contact](actions/delete-contact.md) | `POST /contact/{contactId}/delete` | [docs](https://chatbotkit.com/manuals/contacts) |
| [Delete Conversation](actions/delete-conversation.md) | `POST /conversation/{conversationId}/delete` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Delete Conversation Message](actions/delete-conversation-message.md) | `POST /conversation/{conversationId}/message/{messageId}/delete` | [docs](https://chatbotkit.com/manuals/conversation-messages) |
| [Delete Dataset](actions/delete-dataset.md) | `POST /dataset/{datasetId}/delete` | [docs](https://chatbotkit.com/manuals/datasets) |
| [Delete Dataset Record](actions/delete-dataset-record.md) | `POST /dataset/{datasetId}/record/{recordId}/delete` | [docs](https://chatbotkit.com/manuals/dataset-records) |
| [Dispatch Stateful Completion](actions/dispatch-stateful-completion.md) | `POST /conversation/{conversationId}/dispatch` | [docs](https://chatbotkit.com/manuals/dispatching-stateful-conversations) |
| [Ensure Contact Existence](actions/ensure-contact-existence.md) | `POST /contact/ensure` | [docs](https://chatbotkit.com/manuals/contacts) |
| [Fetch Bot](actions/fetch-bot.md) | `GET /bot/{botId}/fetch` | [docs](https://chatbotkit.com/manuals/bots) |
| [Fetch Contact](actions/fetch-contact.md) | `GET /contact/{contactId}/fetch` | [docs](https://chatbotkit.com/manuals/contacts) |
| [Fetch Conversation](actions/fetch-conversation.md) | `GET /conversation/{conversationId}/fetch` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Fetch Conversation Message](actions/fetch-conversation-message.md) | `GET /conversation/{conversationId}/message/{messageId}/fetch` | [docs](https://chatbotkit.com/manuals/conversation-messages) |
| [Fetch Dataset Record](actions/fetch-dataset-record.md) | `GET /dataset/{datasetId}/record/{recordId}/fetch` | [docs](https://chatbotkit.com/manuals/dataset-records) |
| [List Bots](actions/list-bots.md) | `GET /bot/list` | [docs](https://chatbotkit.com/manuals/bots) |
| [List Contacts](actions/list-contacts.md) | `GET /contact/list` | [docs](https://chatbotkit.com/manuals/contacts) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /conversation/{conversationId}/message/list` | [docs](https://chatbotkit.com/manuals/conversation-messages) |
| [List Conversations](actions/list-conversations.md) | `GET /conversation/list` | [docs](https://chatbotkit.com/manuals/conversations) |
| [List Dataset Records](actions/list-dataset-records.md) | `GET /dataset/{datasetId}/record/list` | [docs](https://chatbotkit.com/manuals/dataset-records) |
| [List Datasets](actions/list-datasets.md) | `GET /dataset/list` | [docs](https://chatbotkit.com/manuals/datasets) |
| [List Files](actions/list-files.md) | `GET /file/list` | [docs](https://chatbotkit.com/manuals/files) |
| [Receive AI Response](actions/receive-ai-response.md) | `POST /conversation/{conversationId}/receive` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Retrieve Dataset](actions/retrieve-dataset.md) | `GET /dataset/{datasetId}/fetch` | [docs](https://chatbotkit.com/manuals/datasets) |
| [Retrieve File Details](actions/retrieve-file-details.md) | `GET /file/{fileId}/fetch` | [docs](https://chatbotkit.com/manuals/files) |
| [Search Dataset](actions/search-dataset.md) | `POST /dataset/{datasetId}/search` | [docs](https://chatbotkit.com/manuals/dataset-search) |
| [Send Conversation Message](actions/send-conversation-message.md) | `POST /conversation/{conversationId}/send` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Update Bot](actions/update-bot.md) | `POST /bot/{botId}/update` | [docs](https://chatbotkit.com/manuals/bots) |
| [Update Contact](actions/update-contact.md) | `POST /contact/{contactId}/update` | [docs](https://chatbotkit.com/manuals/contacts) |
| [Update Conversation](actions/update-conversation.md) | `POST /conversation/{conversationId}/update` | [docs](https://chatbotkit.com/manuals/conversations) |
| [Update Conversation Message](actions/update-conversation-message.md) | `POST /conversation/{conversationId}/message/{messageId}/update` | [docs](https://chatbotkit.com/manuals/conversation-messages) |
| [Update Dataset](actions/update-dataset.md) | `POST /dataset/{datasetId}/update` | [docs](https://chatbotkit.com/manuals/datasets) |
| [Update Dataset Record](actions/update-dataset-record.md) | `POST /dataset/{datasetId}/record/{recordId}/update` | [docs](https://chatbotkit.com/manuals/dataset-records) |
| [Upload File Content](actions/upload-file-content.md) | `POST /file/{fileId}/upload` | [docs](https://chatbotkit.com/manuals/files) |
