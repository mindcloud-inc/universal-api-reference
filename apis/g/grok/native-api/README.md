# Grok: Native API Reference

A consolidated summary of Grok's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.x.ai/developers/rest-api-reference/inference
- **API base URL:** `https://api.x.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.x.ai/developers/quickstart)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Batch Requests to Batch](actions/add-batch-requests-to-batch.md) | `POST /v1/batches/:batch_id/requests` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#add-batch-requests-to-a-batch) |
| [Cancel Processing on Batch](actions/cancel-processing-on-batch.md) | `POST /v1/batches/:batch_id:cancel` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#cancel-processing-on-a-batch) |
| [Create Batch](actions/create-batch.md) | `POST /v1/batches` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#create-a-new-batch) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#chat-completions) |
| [Create Client Secret](actions/create-client-secret.md) | `POST /v1/realtime/client_secrets` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#create-client-secret) |
| [Create New Response](actions/create-new-response.md) | `POST /v1/responses` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#create-new-response) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/:file_id` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#delete-a-file) |
| [Delete Previous Response](actions/delete-previous-response.md) | `DELETE /v1/responses/:response_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#delete-previous-response) |
| [Edit Image](actions/edit-image.md) | `POST /v1/images/edits` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/images#image-edit) |
| [Edit Video](actions/edit-video.md) | `POST /v1/videos/edits` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#video-edit) |
| [Generate Image](actions/generate-image.md) | `POST /v1/images/generations` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/images#image-generation) |
| [Generate Video](actions/generate-video.md) | `POST /v1/videos/generations` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#video-generation) |
| [Get API Key](actions/get-api-key.md) | `GET /v1/api-key` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/other#api-key) |
| [Get Batch](actions/get-batch.md) | `GET /v1/batches/:batch_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#get-batch) |
| [Get Deferred Chat Completions](actions/get-deferred-chat-completions.md) | `GET /v1/chat/deferred-completion/:request_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#get-deferred-chat-completions) |
| [Get File Content](actions/get-file-content.md) | `GET /v1/files/:file_id/content` | [docs](https://docs.x.ai/developers/rest-api-reference/files/download#get-file-content) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /v1/files/:file_id` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#get-file-metadata) |
| [Get Image Generation Model](actions/get-image-generation-model.md) | `GET /v1/image-generation-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-image-generation-model) |
| [Get Language Model](actions/get-language-model.md) | `GET /v1/language-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-language-model) |
| [Get Model](actions/get-model.md) | `GET /v1/models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-model) |
| [Get Processing Results of Batch](actions/get-processing-results-of-batch.md) | `GET /v1/batches/:batch_id/results` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#get-processing-results-of-a-batch) |
| [Get Video Generation Model](actions/get-video-generation-model.md) | `GET /v1/video-generation-models/:model_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#get-video-generation-model) |
| [Get Video Generation Results](actions/get-video-generation-results.md) | `GET /v1/videos/:request_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/videos#get-video-generation-results) |
| [Get Voice](actions/get-voice.md) | `GET /v1/tts/voices/:voice_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#get-voice) |
| [Initialize File Upload](actions/initialize-file-upload.md) | `POST /v1/files:initialize` | [docs](https://docs.x.ai/developers/rest-api-reference/files/upload#initialize-a-file-upload) |
| [List Batch Requests](actions/list-batch-requests.md) | `GET /v1/batches/:batch_id/requests` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-requests-in-a-batch) |
| [List Batches](actions/list-batches.md) | `GET /v1/batches` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batches) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#list-files) |
| [List Image Generation Models](actions/list-image-generation-models.md) | `GET /v1/image-generation-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-image-generation-models) |
| [List Language Models](actions/list-language-models.md) | `GET /v1/language-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-language-models) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-models) |
| [List Video Generation Models](actions/list-video-generation-models.md) | `GET /v1/video-generation-models` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/models#list-video-generation-models) |
| [List Voices](actions/list-voices.md) | `GET /v1/tts/voices` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#list-voices) |
| [Retrieve Previous Response](actions/retrieve-previous-response.md) | `GET /v1/responses/:response_id` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/chat#retrieve-previous-response) |
| [Search Content in Collection](actions/search-content-in-collection.md) | `POST /v1/documents/search` | [docs](https://docs.x.ai/developers/rest-api-reference/collections/search#search-content-in-a-collection) |
| [Text to Speech](actions/text-to-speech.md) | `POST /v1/tts` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/voice#text-to-speech) |
| [Tokenize Text](actions/tokenize-text.md) | `POST /v1/tokenize-text` | [docs](https://docs.x.ai/developers/rest-api-reference/inference/other#tokenize-text) |
| [Update File](actions/update-file.md) | `PUT /v1/files/:file_id` | [docs](https://docs.x.ai/developers/rest-api-reference/files/manage#update-a-files-metadata-or-content) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://docs.x.ai/developers/rest-api-reference/files/upload#upload-a-file) |
| [Upload File in Chunks](actions/upload-file-in-chunks.md) | `POST /v1/files:uploadChunks` | [docs](https://docs.x.ai/developers/rest-api-reference/files/upload#upload-a-file-in-chunks) |
