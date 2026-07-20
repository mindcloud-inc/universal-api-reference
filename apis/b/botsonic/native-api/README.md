# Botsonic: Native API Reference

A consolidated summary of Botsonic's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.botsonic.com/docs/rest-api
- **API base URL:** `https://api.botsonic.ai`

## Authentication

### Bot REST API Token

Botsonic bot REST API token used for generation endpoints. Business-management endpoints require a separate USER-API-KEY credential and are intentionally blocked until that credential is available.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.botsonic.com/docs/rest-api)

### Botsonic API Keys

Botsonic requires two documented API-key credentials: a bot REST API token for generation endpoints and a separate user API key for business-management endpoints.

### Credentials

- **Bot API Token:** `botApiToken` · required · Botsonic bot REST API token used as token or X-BOT-KEY for generation endpoints.
- **User API Key:** `userApiKey` · required · Botsonic User API Key used as USER-API-KEY for business-management endpoints.

Send these headers with each API request:

```http
token: <botApiToken>
X-BOT-KEY: <botApiToken>
USER-API-KEY: <userApiKey>
```

[Official authentication documentation](https://docs.botsonic.com/docs/rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upload URLs](actions/bulk-upload-urls.md) | `POST /v1/business/bot-data/bulk-upsert-urls` | [docs](https://docs.botsonic.com/reference/bulk_upload_urls_v1_business_bot_data_bulk_upsert_urls_post) |
| [Create Bot](actions/create-bot.md) | `POST /v1/business/bot` | [docs](https://docs.botsonic.com/reference/create_bot_v1_business_bot_post) |
| [Create FAQ](actions/create-faq.md) | `POST /v1/business/bot-faq` | [docs](https://docs.botsonic.com/reference/create_single_faq_v1_business_bot_faq_post) |
| [Create Starter Question](actions/create-starter-question.md) | `POST /v1/business/bot-starter-questions` | [docs](https://docs.botsonic.com/reference/create_starter_question_v1_business_bot_starter_questions_post) |
| [Delete Bot](actions/delete-bot.md) | `DELETE /v1/business/bot/:botId` | [docs](https://docs.botsonic.com/reference/delete_bot_v1_business_bot__bot_id__delete) |
| [Delete Bot Data](actions/delete-bot-data.md) | `DELETE /v1/business/bot-data/:dataId` | [docs](https://docs.botsonic.com/reference/delete_bot_data_v1_business_bot_data__data_id__delete) |
| [Delete FAQ](actions/delete-faq.md) | `DELETE /v1/business/bot-faq/:faqId` | [docs](https://docs.botsonic.com/reference/delete_bot_faq_v1_business_bot_faq__faq_id__delete) |
| [Delete Starter Question](actions/delete-starter-question.md) | `DELETE /v1/business/bot-starter-questions/:starterQuestionId` | [docs](https://docs.botsonic.com/reference/delete_starter_question_v1_business_bot_starter_questions__starter_question_id__delete) |
| [End Chat](actions/end-chat.md) | `POST /v1/business/bot-data/conversations/:chatId/end-chat` | [docs](https://docs.botsonic.com/reference/end_chat_v1_business_bot_data_conversations__chat_id__end_chat_post) |
| [Generate Business Response](actions/generate-business-response.md) | `POST /v1/business/botsonic` | [docs](https://docs.botsonic.com/reference/generate_sync_or_streaming_response_v1_business_botsonic_post) |
| [Generate Response](actions/generate-response.md) | `POST /v1/botsonic/generate` | [docs](https://docs.botsonic.com/reference/botsonic_api_v1_botsonic_generate_post) |
| [Get Bot](actions/get-bot.md) | `GET /v1/business/bot/:botId` | [docs](https://docs.botsonic.com/reference/get_specific_bot_v1_business_bot__bot_id__get) |
| [Get Bot API Key](actions/get-bot-api-key.md) | `GET /v1/business/bot/:botId/bot-api-key` | [docs](https://docs.botsonic.com/reference/get_bot_api_key_v1_business_bot__bot_id__bot_api_key_get) |
| [Get Conversation](actions/get-conversation.md) | `GET /v1/business/bot-data/conversations/:chatId` | [docs](https://docs.botsonic.com/reference/get_specific_conversation_v1_business_bot_data_conversations__chat_id__get) |
| [List Bot Data](actions/list-bot-data.md) | `GET /v1/business/bot-data/all` | [docs](https://docs.botsonic.com/reference/get_all_bot_data_v1_business_bot_data_all_get) |
| [List Bots](actions/list-bots.md) | `GET /v1/business/bot/all` | [docs](https://docs.botsonic.com/reference/get_all_bots_v1_business_bot_all_get) |
| [List Conversations](actions/list-conversations.md) | `GET /v1/business/bot-data/conversations/all` | [docs](https://docs.botsonic.com/reference/get_all_conversations_v1_business_bot_data_conversations_all_get) |
| [List FAQs](actions/list-faqs.md) | `GET /v1/business/bot-faq/all` | [docs](https://docs.botsonic.com/reference/get_all_faqs_v1_business_bot_faq_all_get) |
| [List Starter Presets](actions/list-starter-presets.md) | `GET /v1/business/bot-starter-presets/all` | [docs](https://docs.botsonic.com/reference/get_all_starter_presets_by_bot_id_v1_business_bot_starter_presets_all_get-1) |
| [List Starter Questions](actions/list-starter-questions.md) | `GET /v1/business/bot-starter-questions/all` | [docs](https://docs.botsonic.com/reference/get_all_starter_questions_v1_business_bot_starter_questions_all_get) |
| [Update Starter Question](actions/update-starter-question.md) | `PATCH /v1/business/bot-starter-questions/:starterQuestionId` | [docs](https://docs.botsonic.com/reference/update_starter_question_v1_business_bot_starter_questions__starter_question_id__patch) |
| [Upload File](actions/upload-file.md) | `POST /v1/business/bot-data/upload-file` | [docs](https://docs.botsonic.com/reference/upload_file_v1_business_bot_data_upload_file_post) |
| [Upload Text](actions/upload-text.md) | `POST /v1/business/bot-data/upload-text` | [docs](https://docs.botsonic.com/reference/upload_text_v1_business_bot_data_upload_text_post) |
