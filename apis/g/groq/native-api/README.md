# Groq: Native API Reference

A consolidated summary of Groq's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://console.groq.com/docs/api-reference
- **API base URL:** `https://api.groq.com`

## Authentication

### API Key

Authenticate with a Groq API key. MindCloud uses the platform-managed implicit `credentials.apiKey` credential and sends it as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://console.groq.com/docs/quickstart)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch](actions/cancel-batch.md) | `POST /openai/v1/batches/:batch_id/cancel` | [docs](https://console.groq.com/docs/api-reference#batches-cancel) |
| [Create Batch](actions/create-batch.md) | `POST /openai/v1/batches` | [docs](https://console.groq.com/docs/api-reference#batches-create) |
| [Create Chat Completion](actions/create-chat-completion.md) | `POST /openai/v1/chat/completions` | [docs](https://console.groq.com/docs/api-reference#chat-create) |
| [Create Embedding](actions/create-embedding.md) | `POST /openai/v1/embeddings` | [docs](https://console.groq.com/docs/api-reference) |
| [Create Fine Tuning](actions/create-fine-tuning.md) | `POST /v1/fine_tunings` | [docs](https://console.groq.com/docs/api-reference#fine-tuning-create) |
| [Create Reranking](actions/create-reranking.md) | `POST /openai/v1/reranking` | [docs](https://console.groq.com/docs/api-reference) |
| [Create Response](actions/create-response.md) | `POST /openai/v1/responses` | [docs](https://console.groq.com/docs/api-reference#responses-create) |
| [Create Speech](actions/create-speech.md) | `POST /openai/v1/audio/speech` | [docs](https://console.groq.com/docs/api-reference#audio-speech) |
| [Create Transcription](actions/create-transcription.md) | `POST /openai/v1/audio/transcriptions` | [docs](https://console.groq.com/docs/api-reference#audio-transcription) |
| [Create Translation](actions/create-translation.md) | `POST /openai/v1/audio/translations` | [docs](https://console.groq.com/docs/api-reference#audio-translation) |
| [Delete File](actions/delete-file.md) | `DELETE /openai/v1/files/:file_id` | [docs](https://console.groq.com/docs/api-reference#files-delete) |
| [Delete Fine Tuning](actions/delete-fine-tuning.md) | `DELETE /v1/fine_tunings/:id` | [docs](https://console.groq.com/docs/api-reference#fine-tuning-delete) |
| [Delete Model](actions/delete-model.md) | `DELETE /openai/v1/models/:model` | [docs](https://console.groq.com/docs/api-reference#models) |
| [Download File](actions/download-file.md) | `GET /openai/v1/files/:file_id/content` | [docs](https://console.groq.com/docs/api-reference#files-download) |
| [Get Fine Tuning](actions/get-fine-tuning.md) | `GET /v1/fine_tunings/:id` | [docs](https://console.groq.com/docs/api-reference#fine-tuning-get) |
| [List Batches](actions/list-batches.md) | `GET /openai/v1/batches` | [docs](https://console.groq.com/docs/api-reference#batches-list) |
| [List Files](actions/list-files.md) | `GET /openai/v1/files` | [docs](https://console.groq.com/docs/api-reference#files-list) |
| [List Fine Tunings](actions/list-fine-tunings.md) | `GET /v1/fine_tunings` | [docs](https://console.groq.com/docs/api-reference#fine-tuning-list) |
| [List Models](actions/list-models.md) | `GET /openai/v1/models` | [docs](https://console.groq.com/docs/api-reference#models-list) |
| [Retrieve Batch](actions/retrieve-batch.md) | `GET /openai/v1/batches/:batch_id` | [docs](https://console.groq.com/docs/api-reference#batches-retrieve) |
| [Retrieve File](actions/retrieve-file.md) | `GET /openai/v1/files/:file_id` | [docs](https://console.groq.com/docs/api-reference#files-retrieve) |
| [Retrieve Model](actions/retrieve-model.md) | `GET /openai/v1/models/:model` | [docs](https://console.groq.com/docs/api-reference#models-retrieve) |
| [Upload File](actions/upload-file.md) | `POST /openai/v1/files` | [docs](https://console.groq.com/docs/api-reference#files-upload) |
