# xAI: Native API Reference

A consolidated summary of xAI's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.x.ai/developers/rest-api-reference/inference
- **API base URL:** `https://api.x.ai/v1`

## Authentication

### API Key

Authenticate requests with an xAI API key using the Authorization bearer header.

### Credentials

- **xAI API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.x.ai/developers/rest-api-reference/inference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `pagination_token` in the query string as the pagination cursor; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Batch Requests](actions/add-batch-requests.md) | `POST /batches/:batch_id/requests` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#add-batch-requests) |
| [Cancel Batch](actions/cancel-batch.md) | `POST /batches/:batch_id:cancel` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#cancel-batch) |
| [Create Anthropic Message](actions/create-anthropic-message.md) | `POST /messages` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/legacy#create-messages-response) |
| [Create Batch](actions/create-batch.md) | `POST /batches` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#create-batch) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /chat/completions` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-chat-completion) |
| [Create Legacy Text Completion](actions/create-legacy-text-completion.md) | `POST /completions` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/legacy#create-text-completion) |
| [Create Realtime Client Secret](actions/create-realtime-client-secret.md) | `POST /realtime/client_secrets` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#create-realtime-client-secret) |
| [Create Response](actions/create-response.md) | `POST /responses` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-new-response) |
| [Create Text To Speech](actions/create-text-to-speech.md) | `POST /tts` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#text-to-speech) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:file_id` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#delete-file) |
| [Delete Response](actions/delete-response.md) | `DELETE /responses/:response_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#delete-response) |
| [Download File Content](actions/download-file-content.md) | `GET /files/:file_id/content` | [docs](https://docs.x.ai/developers/rest-api-reference/files/download#download-file-content) |
| [Edit Image](actions/edit-image.md) | `POST /images/edits` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/images#image-edit) |
| [Edit Video](actions/edit-video.md) | `POST /videos/edits` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#edit-video) |
| [Extend Video](actions/extend-video.md) | `POST /videos/extensions` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#extend-video) |
| [Generate Image](actions/generate-image.md) | `POST /images/generations` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/images#image-generation) |
| [Generate Video](actions/generate-video.md) | `POST /videos/generations` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#generate-video) |
| [Get Batch](actions/get-batch.md) | `GET /batches/:batch_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#get-batch) |
| [Get Deferred Chat Completion](actions/get-deferred-chat-completion.md) | `GET /chat/deferred-completion/:request_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#get-deferred-chat-completion) |
| [Get Image Generation Model](actions/get-image-generation-model.md) | `GET /image-generation-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-image-generation-model) |
| [Get Language Model](actions/get-language-model.md) | `GET /language-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-language-model) |
| [Get Model](actions/get-model.md) | `GET /models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-model) |
| [Get TTS Voice](actions/get-tts-voice.md) | `GET /tts/voices/:voice_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#get-tts-voice) |
| [Get Video Generation Model](actions/get-video-generation-model.md) | `GET /video-generation-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-video-generation-model) |
| [Get Video Result](actions/get-video-result.md) | `GET /videos/:request_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#get-video-result) |
| [List Batch Requests](actions/list-batch-requests.md) | `GET /batches/:batch_id/requests` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-requests) |
| [List Batch Results](actions/list-batch-results.md) | `GET /batches/:batch_id/results` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-results) |
| [List Batches](actions/list-batches.md) | `GET /batches` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batches) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#list-files) |
| [List Image Generation Models](actions/list-image-generation-models.md) | `GET /image-generation-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-image-generation-models) |
| [List Language Models](actions/list-language-models.md) | `GET /language-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-language-models) |
| [List Models](actions/list-models.md) | `GET /models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-models) |
| [List TTS Voices](actions/list-tts-voices.md) | `GET /tts/voices` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#list-tts-voices) |
| [List Video Generation Models](actions/list-video-generation-models.md) | `GET /video-generation-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-video-generation-models) |
| [Retrieve File](actions/retrieve-file.md) | `GET /files/:file_id` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#retrieve-file) |
| [Retrieve Response](actions/retrieve-response.md) | `GET /responses/:response_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#retrieve-response) |
| [Search Documents](actions/search-documents.md) | `POST /documents/search` | [docs](https://docs.x.ai/developers/rest-api-reference/collections/search#search-documents) |
