# Insighto.ai: Native API Reference

A consolidated summary of Insighto.ai's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.insighto.ai/api-reference
- **OpenAPI specification:** https://api.insighto.ai/api/v1/openapi.json
- **API base URL:** `https://api.insighto.ai/api/v1`

## Authentication

### API Key

Authenticate with an Insighto.ai API key generated from Settings > API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.insighto.ai/api-reference/form/create-form)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `items`. The total page count is read from `pages`. The current page number is read from `page`.

## Pagination

Use `size` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Datasourcefile](actions/add-datasource-file.md) | `POST /datasource/:datasource_id/file` | [docs](https://docs.insighto.ai/api-reference/data-source/add-datasourcefile) |
| [Add Datasourcefile Text Blob](actions/add-datasource-text-blob.md) | `POST /datasource/:datasource_id/text_blob` | [docs](https://docs.insighto.ai/api-reference/data-source/add-datasourcefile-text-blob) |
| [Add Datasource To Assistant](actions/add-datasource-to-assistant.md) | `POST /assistant/:assistant_id/data_source/:datasource_id` | [docs](https://docs.insighto.ai/api-reference/assistant/add-datasource-to-assistant) |
| [Add Intent To Assistant](actions/add-intent-to-assistant.md) | `POST /assistant/:assistant_id/intent/:intent_id` | [docs](https://docs.insighto.ai/api-reference/assistant/add-intent-to-assistant) |
| [Create Assistant](actions/create-assistant.md) | `POST /assistant` | [docs](https://docs.insighto.ai/api-reference/assistant/create-assistant) |
| [Create Data Source](actions/create-data-source.md) | `POST /datasource` | [docs](https://docs.insighto.ai/api-reference/data-source/create-data-source) |
| [Create Intent](actions/create-intent.md) | `POST /intent` | [docs](https://docs.insighto.ai/api-reference/intent/create-intent) |
| [Create Widget](actions/create-widget.md) | `POST /widget` | [docs](https://docs.insighto.ai/api-reference/widget/create-widget) |
| [Delete Assistant By Id](actions/delete-assistant-by-id.md) | `DELETE /assistant/:assistant_id` | [docs](https://docs.insighto.ai/api-reference/assistant/delete-assistant-by-id) |
| [Delete Datasource By Id](actions/delete-datasource-by-id.md) | `DELETE /datasource/:datasource_id` | [docs](https://docs.insighto.ai/api-reference/data-source/delete-datasource-by-id) |
| [Delete Widget By Id](actions/delete-widget-by-id.md) | `DELETE /widget/:widget_id` | [docs](https://docs.insighto.ai/api-reference/widget/delete-widget-by-id) |
| [Get Assistant By Id](actions/get-assistant-by-id.md) | `GET /assistant/:assistant_id` | [docs](https://docs.insighto.ai/api-reference/assistant/get-assistant-by-id) |
| [Get Contact By Id](actions/get-contact-by-id.md) | `GET /contact/:contact_id` | [docs](https://docs.insighto.ai/api-reference/contact/get-contact-by-id) |
| [Get Conversation By Id](actions/get-conversation-by-id.md) | `GET /conversation/:conversation_id` | [docs](https://docs.insighto.ai/api-reference/conversation/get-conversation-by-id) |
| [Get Transcript Of A Conversation](actions/get-conversation-transcript.md) | `GET /conversation/:conversation_id/transcript` | [docs](https://docs.insighto.ai/api-reference/conversation/get-transcript-of-a-conversation) |
| [Get Datasource By Id](actions/get-datasource-by-id.md) | `GET /datasource/:datasource_id` | [docs](https://docs.insighto.ai/api-reference/data-source/get-datasource-by-id) |
| [Get Intent By Id](actions/get-intent-by-id.md) | `GET /intent/:intent_id` | [docs](https://docs.insighto.ai/api-reference/intent/get-intent-by-id) |
| [Get Widget By Id](actions/get-widget-by-id.md) | `GET /widget/:widget_id` | [docs](https://docs.insighto.ai/api-reference/widget/get-widget-by-id) |
| [List Assistants](actions/list-assistants.md) | `GET /assistant` | [docs](https://docs.insighto.ai/api-reference/assistant/get-list-of-assistants) |
| [List Contacts](actions/list-contacts.md) | `GET /contact` | [docs](https://docs.insighto.ai/api-reference/contact/get-list-of-contacts) |
| [List Conversations](actions/list-conversations.md) | `GET /conversation` | [docs](https://docs.insighto.ai/api-reference/conversation/get-list-of-conversations) |
| [Get List Of Conversations By Contact Id](actions/list-conversations-by-contact-id.md) | `GET /conversation/by-contact/:contact_id` | [docs](https://docs.insighto.ai/api-reference/conversation/get-list-of-conversations-by-contact-id) |
| [List Data Source Files For Data Source Id](actions/list-data-source-files-by-datasource-id.md) | `GET /datasource/:datasource_id/data_source_files` | [docs](https://docs.insighto.ai/api-reference/data-source/get-list-of-data-source-files-for-data-source-id) |
| [List Data Sources](actions/list-data-sources.md) | `GET /datasource` | [docs](https://docs.insighto.ai/api-reference/data-source/get-list-of-data-sources) |
| [List Intents](actions/list-intents.md) | `GET /intent/list` | [docs](https://docs.insighto.ai/api-reference/intent/read-intents-list) |
| [List Widgets](actions/list-widgets.md) | `GET /widget` | [docs](https://docs.insighto.ai/api-reference/widget/get-list-of-widgets) |
| [Update Assistant By Id](actions/update-assistant-by-id.md) | `PUT /assistant/:assistant_id` | [docs](https://docs.insighto.ai/api-reference/assistant/update-assistant-by-id) |
| [Update Contact By Id](actions/update-contact-by-id.md) | `PUT /contact/:contact_id` | [docs](https://docs.insighto.ai/api-reference/contact/update-contact-by-id) |
| [Update Widget By Id](actions/update-widget-by-id.md) | `PUT /widget/:widget_id` | [docs](https://docs.insighto.ai/api-reference/widget/update-widget-by-id) |
| [Upsert Contact By Email Or Phone Number](actions/upsert-contact-by-email-or-phone-number.md) | `POST /contact/upsert` | [docs](https://docs.insighto.ai/api-reference/contact/upsert-contact-by-email-or-phone-number) |
