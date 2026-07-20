# Open AI: Native API Reference

A consolidated summary of Open AI's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://developers.openai.com/api/
- **OpenAPI specification:** https://raw.githubusercontent.com/openai/openai-openapi/master/openapi.yaml
- **API base URL:** `https://api.openai.com`

## Authentication

### API Key

OpenAI API key sent as a Bearer token in the Authorization header for every API request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://platform.openai.com/docs/api-reference/authentication)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add File To Vector Store](actions/add-file-to-vector-store.md) | `POST v1/vector_stores/:vector_store_id/files` | [docs](https://developers.openai.com/api/reference/resources/vector_stores/subresources/files/methods/create) |
| [Cancel Batch](actions/cancel-batch.md) | `POST v1/batches/:batch_id/cancel` | [docs](https://developers.openai.com/api/reference/resources/batches/methods/cancel) |
| [Cancel Response](actions/cancel-response.md) | `POST v1/responses/:response_id/cancel` | [docs](https://developers.openai.com/api/reference/resources/responses/methods/cancel) |
| [Compact Response](actions/compact-response.md) | `POST v1/responses/compact` | [docs](https://developers.openai.com/api/reference/overview) |
| [Count Response Input Tokens](actions/count-response-input-tokens.md) | `POST v1/responses/input_tokens` | [docs](https://developers.openai.com/api/reference/overview) |
| [Create Batch](actions/create-batch.md) | `POST v1/batches` | [docs](https://developers.openai.com/api/reference/resources/batches/methods/create) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST v1/chat/completions` | [docs](https://developers.openai.com/api/reference/resources/chat) |
| [Create Conversation](actions/create-conversation.md) | `POST v1/conversations` | [docs](https://developers.openai.com/api/reference/overview) |
| [Create Conversation Item](actions/create-conversation-item.md) | `POST v1/conversations/:conversation_id/items` | [docs](https://developers.openai.com/api/reference/overview) |
| [Create Embedding](actions/create-embedding.md) | `POST v1/embeddings` | [docs](https://developers.openai.com/api/reference/resources/embeddings/methods/create) |
| [Create Response](actions/create-response.md) | `POST v1/responses` | [docs](https://developers.openai.com/api/reference/resources/responses/methods/create) |
| [Create Transcription](actions/create-transcription.md) | `POST v1/audio/transcriptions` | [docs](https://developers.openai.com/api/reference/resources/audio/subresources/transcriptions/methods/create) |
| [Create Translation](actions/create-translation.md) | `POST v1/audio/translations` | [docs](https://developers.openai.com/api/reference/resources/audio/subresources/translations/methods/create) |
| [Create Vector Store](actions/create-vector-store.md) | `POST v1/vector_stores` | [docs](https://developers.openai.com/api/reference/resources/vector_stores/methods/create) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE v1/conversations/:conversation_id` | [docs](https://developers.openai.com/api/reference/overview) |
| [Delete Conversation Item](actions/delete-conversation-item.md) | `DELETE v1/conversations/:conversation_id/items/:item_id` | [docs](https://developers.openai.com/api/reference/conversations/delete-item) |
| [Delete File](actions/delete-file.md) | `DELETE v1/files/:file_id` | [docs](https://developers.openai.com/api/reference/files/delete) |
| [Delete Response](actions/delete-response.md) | `DELETE v1/responses/:response_id` | [docs](https://developers.openai.com/api/reference/resources/responses/methods/delete) |
| [Delete Vector Store](actions/delete-vector-store.md) | `DELETE v1/vector_stores/:vector_store_id` | [docs](https://developers.openai.com/api/reference/vector-stores/delete) |
| [Delete Vector Store File](actions/delete-vector-store-file.md) | `DELETE v1/vector_stores/:vector_store_id/files/:file_id` | [docs](https://developers.openai.com/api/reference/vector-stores-files/delete) |
| [Generate Image](actions/generate-image.md) | `POST v1/images/generations` | [docs](https://developers.openai.com/api/reference/resources/images/methods/generate) |
| [Get Conversation](actions/get-conversation.md) | `GET v1/conversations/:conversation_id` | [docs](https://developers.openai.com/api/reference/overview) |
| [Get Conversation Item](actions/get-conversation-item.md) | `GET v1/conversations/:conversation_id/items/:item_id` | [docs](https://developers.openai.com/api/reference/overview) |
| [Get File](actions/get-file.md) | `GET v1/files/:file_id` | [docs](https://developers.openai.com/api/reference/files/retrieve) |
| [Get File Content](actions/get-file-content.md) | `GET v1/files/:file_id/content` | [docs](https://developers.openai.com/api/reference/files/retrieve-contents) |
| [Get Response](actions/get-response.md) | `GET v1/responses/:response_id` | [docs](https://developers.openai.com/api/reference/resources/responses/methods/retrieve) |
| [Get Vector Store](actions/get-vector-store.md) | `GET v1/vector_stores/:vector_store_id` | [docs](https://developers.openai.com/api/reference/vector-stores/retrieve) |
| [Get Vector Store File](actions/get-vector-store-file.md) | `GET v1/vector_stores/:vector_store_id/files/:file_id` | [docs](https://developers.openai.com/api/reference/vector-stores-files/retrieve) |
| [Get Vector Store File Content](actions/get-vector-store-file-content.md) | `GET v1/vector_stores/:vector_store_id/files/:file_id/content` | [docs](https://developers.openai.com/api/reference/vector-stores-files/retrieve-content) |
| [List Conversation Items](actions/list-conversation-items.md) | `GET v1/conversations/:conversation_id/items` | [docs](https://developers.openai.com/api/reference/overview) |
| [List Files](actions/list-files.md) | `GET v1/files` | [docs](https://developers.openai.com/api/reference/files/list) |
| [List Models](actions/list-models.md) | `GET v1/models` | [docs](https://developers.openai.com/api/reference/resources/models/methods/list) |
| [List Response Input Items](actions/list-response-input-items.md) | `GET v1/responses/:response_id/input_items` | [docs](https://developers.openai.com/api/reference/resources/responses/subresources/input_items/methods/list) |
| [List Vector Store Files](actions/list-vector-store-files.md) | `GET v1/vector_stores/:vector_store_id/files` | [docs](https://developers.openai.com/api/reference/vector-stores-files/list) |
| [List Vector Stores](actions/list-vector-stores.md) | `GET v1/vector_stores` | [docs](https://developers.openai.com/api/reference/vector-stores/list) |
| [Moderate Input](actions/moderate-input.md) | `POST v1/moderations` | [docs](https://developers.openai.com/api/reference/resources/moderations/methods/create) |
| [Retrieve Batch](actions/retrieve-batch.md) | `GET v1/batches/:batch_id` | [docs](https://developers.openai.com/api/reference/resources/batches/methods/retrieve) |
| [Retrieve Model](actions/retrieve-model.md) | `GET v1/models/:model` | [docs](https://developers.openai.com/api/reference/resources/models/methods/retrieve) |
| [Search Vector Store](actions/search-vector-store.md) | `POST v1/vector_stores/:vector_store_id/search` | [docs](https://developers.openai.com/api/reference/resources/vector_stores/methods/search) |
| [Update Conversation](actions/update-conversation.md) | `POST v1/conversations/:conversation_id` | [docs](https://developers.openai.com/api/reference/overview) |
| [Update Vector Store](actions/update-vector-store.md) | `POST v1/vector_stores/:vector_store_id` | [docs](https://developers.openai.com/api/reference/vector-stores/modify) |
| [Upload File](actions/upload-file.md) | `POST v1/files` | [docs](https://developers.openai.com/api/reference/resources/files/methods/create) |
