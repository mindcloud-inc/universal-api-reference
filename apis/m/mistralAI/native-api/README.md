# Mistral AI: Native API Reference

A consolidated summary of Mistral AI's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://docs.mistral.ai/api
- **OpenAPI specification:** https://docs.mistral.ai/openapi.yaml
- **API base URL:** `https://api.mistral.ai`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.mistral.ai/getting-started/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Agents Completion](actions/agents-completion.md) | `POST /v1/agents/completions` | [docs](https://docs.mistral.ai/api/endpoint/agents#operation-agents_completion_v1_agents_completions_post) |
| [Cancel Batch Job](actions/cancel-batch-job.md) | `POST /v1/batch/jobs/:job_id/cancel` | [docs](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_cancel_batch_job) |
| [Chat Completion](actions/chat-completion.md) | `POST /v1/chat/completions` | [docs](https://docs.mistral.ai/api/endpoint/chat#operation-chat_completion_v1_chat_completions_post) |
| [Chat Moderations](actions/chat-moderations.md) | `POST /v1/chat/moderations` | [docs](https://docs.mistral.ai/api/endpoint/classifiers#operation-chat_moderations_v1_chat_moderations_post) |
| [Create Batch Job](actions/create-batch-job.md) | `POST /v1/batch/jobs` | [docs](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_create_batch_job) |
| [Create Transcription](actions/create-transcription.md) | `POST /v1/audio/transcriptions` | [docs](https://docs.mistral.ai/api/endpoint/audio/transcriptions#operation-audio_api_v1_transcriptions_post) |
| [Delete File](actions/delete-file.md) | `DELETE /v1/files/:file_id` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_delete_file) |
| [Delete Fine Tuned Model](actions/delete-fine-tuned-model.md) | `DELETE /v1/models/:model_id` | [docs](https://docs.mistral.ai/api/endpoint/models#operation-delete_model_v1_models_model_id_delete) |
| [Download File](actions/download-file.md) | `GET /v1/files/:file_id/content` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_download_file) |
| [Embeddings](actions/embeddings.md) | `POST /v1/embeddings` | [docs](https://docs.mistral.ai/api/endpoint/embeddings#operation-embeddings_v1_embeddings_post) |
| [FIM Completion](actions/fim-completion.md) | `POST /v1/fim/completions` | [docs](https://docs.mistral.ai/api/endpoint/fim#operation-fim_completion_v1_fim_completions_post) |
| [Get Batch Job](actions/get-batch-job.md) | `GET /v1/batch/jobs/:job_id` | [docs](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_get_batch_job) |
| [Get Signed URL](actions/get-signed-url.md) | `GET /v1/files/:file_id/url` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_get_signed_url) |
| [List Batch Jobs](actions/list-batch-jobs.md) | `GET /v1/batch/jobs` | [docs](https://docs.mistral.ai/api/endpoint/batch#operation-jobs_api_routes_batch_get_batch_jobs) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_list_files) |
| [List Models](actions/list-models.md) | `GET /v1/models` | [docs](https://docs.mistral.ai/api/endpoint/models#operation-list_models_v1_models_get) |
| [Moderations](actions/moderations.md) | `POST /v1/moderations` | [docs](https://docs.mistral.ai/api/endpoint/classifiers#operation-moderations_v1_moderations_post) |
| [OCR](actions/ocr.md) | `POST /v1/ocr` | [docs](https://docs.mistral.ai/api/endpoint/ocr#operation-ocr_v1_ocr_post) |
| [Retrieve File](actions/retrieve-file.md) | `GET /v1/files/:file_id` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_retrieve_file) |
| [Retrieve Model](actions/retrieve-model.md) | `GET /v1/models/:model_id` | [docs](https://docs.mistral.ai/api/endpoint/models#operation-retrieve_model_v1_models_model_id_get) |
| [Update Fine Tuned Model](actions/update-fine-tuned-model.md) | `PATCH /v1/fine_tuning/models/:model_id` | [docs](https://docs.mistral.ai/api/endpoint/models#operation-jobs_api_routes_fine_tuning_update_fine_tuned_model) |
| [Upload File](actions/upload-file.md) | `POST /v1/files` | [docs](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_upload_file) |
